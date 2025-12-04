# Sequence Diagram: Message Flow

![Sequence Diagram](assets/sequence_diagram.png)

**Flow:**
1. User logs in → Channel API `/messages/unread`
2. Process API orchestrates:
   - SystemAPI_Messages → fetch raw messages
   - SystemAPI_UserPrefs → fetch user preferences
   - BulkAggregation API → aggregate bulk messages
3. Apply validation & transformations
4. Trigger push notifications for messages with `pushNotification: true`
5. Return messages to client → cache unread IDs & show totalUnread
6. User clicks a message → `/messages/{id}` → Process API returns full content
7. Channel API → Process API: PATCH `/messages/{id}/read` → update unread count & stop notifications
