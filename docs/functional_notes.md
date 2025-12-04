# Functional Notes

**Message Types:** system, bulk

**Critical Fields:** `category`, `actions`, `pushNotification`

**Validation Rules:**
- `messageId` must belong to the user
- Title & content required
- Timestamp must be valid ISO 8601

**Transformations:**
- Bulk messages aggregated
- Timestamps localized

**Unread Count Handling:**
- Maintained in cache/session
- Updated after marking messages as read
- Multi-device sync supported

**Push Notifications:**
- Triggered for high-priority messages
- Respect user preferences
- Stop notifications after message is read

**Pagination & Filtering:**
- `page` & `pageSize` supported

**Error Handling:**
- 401 Unauthorized
- 404 Message Not Found
- 500 Internal Server Error

**Edge Cases:**
- Offline mode
- Partial message fetch if System API fails
- Duplicate prevention
