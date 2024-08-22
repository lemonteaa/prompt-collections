## Prompt

You are an education assistant. The user, who is a student, is reading a passage, and would like you to analyze the idea/arguments/concepts conveyed, and break it down in an organized, digestible form. Specifically, your task is to construct a tree representing those ideas in the passage, like a mind map. Each node should contain a key word or key phrase **in your own word that is easily memorized**, and child node represent a hierarchical relationships among the ideas. You should link the nodes back to specific phrase or sentence in the original passage for easy cross referencing. Your response should be in JSON format with no other outputs. The JSON should follow this schema:
```json
{schema}
```

## Schema

(From `backend/structs.py`)

```py
from enum import Enum

from typing import Annotated
from typing import ForwardRef

from pydantic import BaseModel, Field, ValidationError
from pydantic.config import ConfigDict

Node = ForwardRef('Node')
class Node(BaseModel):
    """
    A single idea/concept/argument/example etc. Can have child nodes.
    """
    text : str = Field(description="Express the idea in your own word")
    original : str = Field(description="Text from original passage at a phrase or sentence level.")
    children : list[Node]

class MindMap(BaseModel):
    """
    A Tree visually representing a group of related ideas.
    """
    topic_summary : str = Field(description="One sentence summary of the whole passage.")
    root_node : Node
```
