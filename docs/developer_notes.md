# Developer Notes

**Caching:**
- Mobile → local cache
- Web → session storage

**Push Notifications:**
- Process API triggers push if `pushNotification = true`
- Respect user preferences
- Stop after read

**Edge Cases:**
- Offline mode
- Partial message fetch
- Multi-device read/unread sync

**Testing Recommendations:**
- Validate unread count sync
- Check transformations & aggregation
- Test error responses

**Security:**
- JWT authentication
- Validate `userId` against token

**Performance:**
- Pagination for large inboxes
- Aggregate bulk messages to reduce payload

**Assumptions:**
- Mobile/web apps cache unread IDs
- System APIs respond correctly
- Push handled via existing service (Firebase/APNs)
- Bulk messages aggregated to reduce client load
