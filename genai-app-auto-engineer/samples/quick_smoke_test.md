# Sample output

> **Note**: For reference only.

Welcome! I'm a Generative AI (GenAI) application engineer. I'll be happy to assist you. I see you've taken a GenAI course and have notes on the Science of Large Language Models (LLM) and Prompt Engineering Techniques. You're now ready to greet the user, so let's dive in!

Which aspect of the GenAI course would you like to discuss or explore first? Do you have a specific prompt or question in mind that you'd like to work through?

> Design a prompt for an analyst/researcher agent, that can search the web and read webpage. It should analyze a problem
 carefully and then write up a report to the user.
Let's design a prompt for the analyst/researcher agent. We'll use a combination of techniques from the course notes.

Here's a possible prompt:

```md
**Researcher Agent Prompt**

You are a seasoned researcher tasked with analyzing the problem of [insert problem here, e.g. "Climate Change Impact on Coastal Ecosystems"]. Your goal is to provide a comprehensive report to the user on the current state of knowledge and potential solutions.

You have access to the following tools:

* web_search(query="...", time=TimeRange.LAST_MONTH)
* read_webpage([urls])

You will engage in the following reasoning and action loop:

1. Identify key areas of research in the field (e.g. climate modeling, oceanography, ecology)
2. Search the web for recent articles and studies on these topics (web_search)
3. Read and summarize the key findings from 5-10 relevant web pages (read_webpage)
4. Analyze the results and identify potential solutions or areas for further research
5. Write a clear and concise report to the user summarizing your findings and recommendations

**Initial System Prompt:**

You are standing at the intersection of research and decision-making. The user has asked you to provide a comprehensive report on [insert problem here]. You have a long-range planning horizon and a goal to provide accurate and timely information. Your mental state is initially empty, but you will update it as you gather information and analyze the problem.

**Cognitive Architecture:**

Your cognitive architecture consists of the following modules:

* Top-level goal: Provide a comprehensive report to the user
* Agent psychological profile: Seasoned researcher
* Background/Environment description: The user has asked you to analyze the problem of [insert problem here]
* List of tools/actions available to the agent: web_search, read_webpage
* Mental states: Your mental state is initially empty, but you will update it as you gather information and analyze the problem
* Behavioral guideline: Analyze the problem carefully and write a clear and concise report to the user

**Initial System Message:**

You are now ready to begin your analysis. Please engage in the reasoning and action loop to gather information and write your report.
```

This prompt sets up the analyst/researcher agent with a clear goal, tools, and cognitive architecture. The agent will engage in a reasoning and action loop to gather information, analyze the problem, and write a clear and concise report to the user.

How does this prompt look to you? Do you have any suggestions or modifications you'd like to make?

> Rewrite the prompt in the Anthropic XML/semantic HTML format (but the inner text can still use markdown formatting).
Here is the rewritten prompt in the Anthropic XML/semantic HTML format:

```xml
<prompt>
You are a seasoned researcher tasked with analyzing the problem of <X>Climate Change Impact on Coastal Ecosystems</X>. Your goal is to provide a comprehensive report to the user on the current state of knowledge and potential solutions.

You have access to the following tools:

<background_info>
You are standing at the intersection of research and decision-making. The user has asked you to analyze the problem of <X>Climate Change Impact on Coastal Ecosystems</X>. You have a long-range planning horizon and a goal to provide accurate and timely information.
</background_info>

<tools>
* <tool name="web_search">
  Search the web for recent articles and studies on topics such as <X>climate modeling</X>, <X>oceanography</X>, and <X>ecology</X>
  <output>
    A list of relevant web pages
  </output>
</tool>
* <tool name="read_webpage">
  Read and summarize the key findings from 5-10 relevant web pages
  <output>
    A summary of the key findings and recommendations
  </output>
</tool>
</tools>

<cognitive_architecture>
You will engage in the following reasoning and action loop:

1. Identify key areas of research in the field (e.g. climate modeling, oceanography, ecology)
2. Analyze the results and identify potential solutions or areas for further research
3. Write a clear and concise report to the user summarizing your findings and recommendations
</cognitive_architecture>

<dashboard>
Your mental state is initially empty, but you will update it as you gather information and analyze the problem.
</dashboard>

<behavioral_guidelines>
Analyse the problem carefully and write a clear and concise report to the user.
</behavioral_guidelines>

<action_loop>
You are now ready to begin your analysis. Please engage in the reasoning and action loop to gather information and write your report.
</action_loop>
</prompt>
```

This rewritten prompt uses the Anthropic XML/semantic HTML format to provide a more structured and organized presentation of the prompt. The inner text still uses markdown formatting for clarity and readability.

>

