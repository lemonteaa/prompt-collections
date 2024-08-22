# prompt-collections

This is my personal (incomplete) collections of prompts, with a focus on LLM GenAI app development (but also some unrelated fun too).

## Lessons learned

- Anthropic's Custom XML tag for structured output in general is quite useful and can be competitive to JSON, especially for more complex scenarios. Although it's more verbose, its advantages include:
  - Can handle more complex data: XML tag supports attributes which can be thought of as metadata.
  - And the body inside a tag can be text interleaved with tag, so hybrid natural language/structured data use case are quite suitable.
- Revising the basics of prompt engineering technique that I thought I mastered long ago can be beneficial:
  - Like they say, practise makes perfect
  - A simple combination of Chain of Thought + Few shot in context learning can be powerful, but also have diverse applications
- Chats that want rich behavior but also reliability, plus some limited forms of agentic behavior, can benefits from the point above:
  - So Chain of thought and ReACT are related, but also, within a chat context, ReACT can be turned into a per-turn single round things which may makes it easier on the bot (i.e. each conversation turn, ask AI to always do exactly one round of ReACT (implicitly), but can expand the space of data being acted on from a single action, into complex, composite actions that modify the whole state space)
- Random research paper: you can in context teach the use of general simple skills too, so Chain of Thoughts is not limited to Math. Especially attractive would be the potential to improve agentic capability through improving planning and reasoning.
- Lessons of Chatbot pre-ChatGPT era might be useful too (i.e. infer user intent, mood, etc explicitly)
