## Unread Messages Example

```json
{
  "totalUnread": 4,
  "messages": [
    {
      "messageId": "12345",
      "title": "Address Change Confirmation",
      "summary": "Your address has been updated successfully",
      "type": "system",
      "status": "unread",
      "timestamp": "2025-12-04T09:15:00Z",
      "category": "Account",
      "actions": ["acknowledge"],
      "pushNotification": true
    },
    {
      "messageId": "67890",
      "title": "Dividend Applied",
      "summary": "Dividends applied for December for your portfolio",
      "type": "bulk",
      "status": "unread",
      "timestamp": "2025-12-04T08:00:00Z",
      "category": "Finance",
      "actions": ["download"],
      "pushNotification": false
    }
  ]
}

```