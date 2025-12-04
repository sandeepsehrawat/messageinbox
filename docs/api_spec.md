# API Specification (OpenAPI)

The full OpenAPI YAML is included in the repo: [1_OpenAPI_Spec.yaml](../1_OpenAPI_Spec.yaml)

**Endpoints:**
- `GET /messages/unread` → fetch unread messages
- `GET /messages/{messageId}` → fetch full message content
- `PATCH /messages/{messageId}` → mark message as read

**Key Fields:**
- `messageId` (string, required)
- `title` / `content` (string, required)
- `type` (`system` | `bulk`)
- `status` (`read` | `unread`)
- `timestamp` (ISO 8601)
- `category` (string)
- `actions` (array of strings: download, acknowledge)
- `pushNotification` (boolean)
