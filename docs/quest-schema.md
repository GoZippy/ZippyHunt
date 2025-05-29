# Quest JSON Schema – ZippyQuest

This file defines the data structure used to generate, validate, and deploy quests in the ZippyQuest backend.

---

## 🧱 Base Structure

```json
{
  "id": "string",
  "title": "string",
  "description": "string",
  "location": {
    "latitude": "float",
    "longitude": "float",
    "address": "string"
  },
  "quest_type": "location | trivia | photo | puzzle | sponsor",
  "difficulty": 1,
  "age_rating": "all | 13+ | 16+ | 21+",
  "required_class": ["ranger", "sage", "merchant", "scout"],
  "faction_alignment": "light | dark | neutral",
  "rewards": {
    "xp": "integer",
    "loot": ["badge_id", "item_id", "coupon_id"]
  },
  "requirements": {
    "check_in": true,
    "qr_code": false,
    "photo_submission": false
  },
  "timing": {
    "available_from": "ISO 8601 date",
    "available_until": "ISO 8601 date"
  },
  "storyline": "string (optional)"
}
