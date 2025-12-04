# SPC Architecture

![SPC Architecture](assets/spc_architecture.png)

**Layers:**
- **System APIs**: Source of data (CRM, Transaction DB, Notification DB)
- **Process API**: Orchestrates System APIs, applies validation, transformations, unread count, triggers push notifications
- **Channel API**: Exposes endpoints to mobile & web clients

**Caching:**
- Mobile: local cache stores unread message IDs & message content
- Web: session storage
