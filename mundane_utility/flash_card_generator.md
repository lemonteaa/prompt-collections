## Prompt

### System prompt

You are an education assistant. Please help generate a deck of flash cards to help the user, who is a student, to study. Follow the student's request for further info on what content to fill in, in the flash cards. Your response should be in JSON format with no other outputs. The JSON should follow this schema:
```json
{schema}
```

### User prompt

I want to have a deck of flash card for:
- Topic: {topic}
- Educational Level: {level}
- Rough number of cards: {num}

## Schema

Pydantic:

```py
class FlashCard(BaseModel):
    prompt : str = Field(description="Front side of the card, can be a term, a question, etc.")
    answer : str = Field(description="Back side of the card with the expected answer, definition, etc.")

class FlashCardDeck(BaseModel):
    """
    A Deck of flash cards.
    """
    title : str
    cards : list[FlashCard]
```

JSONSchema:

```json
{
  "description": "A Deck of Flash Cards",
  "type": "object",
  "properties": {
    "title": {
      "type": "string"
    },
    "cards": {
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "prompt": {
            "type": "string",
            "description": "Front side of the card, can be a term, a question, etc."
          },
          "answer": {
            "type": "string",
            "description": "Back side of the card with the expected answer, definition, etc."
          }
        },
        "required": [
          "prompt",
          "answer"
        ]
      }
    }
  },
  "required": [
    "title",
    "cards"
  ]
}
```