# Awesome Prompt Engineering
{Awesome Works in Progress}

`Designing a good prompt is like giving clear instructions to a very smart assistant.
The clearer and more structured you are, the better the output you receive.`

## Prompt Key Elements
* **Clear Objective**: Know the purpose of your prompt. Is it to elicit a narrative, gather information, prompt a creative response, or test knowledge?
* **Specificity**: Be as specific as possible to guide the response. Vague prompts can lead to off-topic responses.
* **Context and Background**: Include enough context so the respondent understands the situation or topic without needing external information.
* **Clarity**: The language should be straightforward and unambiguous to avoid confusion.
* **Open-Ended Questions**: For creative or analytical responses, open-ended questions can encourage more detailed and thoughtful replies.
* **Guidelines and Constraints**: Clearly outline any guidelines or constraints, such as word count, format, or the type of information you're seeking.
* **Relevance and Interest**: Make sure the prompt is relevant to the audience's interests and knowledge to keep them engaged.
* **Flexibility**: Allow for some level of interpretation or personal input so that the response can be personalized.
* **Feedback Criteria**: If the response will be evaluated, provide criteria for what constitutes a good response.
* **Examples**: Offering examples can clarify expectations and provide a model for the structure and depth of the desired response.
* **Encouragement of Critical Thinking and Creativity**: Especially in educational settings, prompts should encourage users to think critically and creatively.

-----

## Prompt Engineering Tutorial
### 1. Set the Role (Optional but Powerful)
* Assigning a role helps the model understand how to behave and what tone to adopt.
* `Example: You are a senior data analyst specializing in Power BI and data visualization.`

### 2. Define the Goal / Task Clearly
* State exactly what you want the model to do.
* `Your task is to generate three scenario-based MCQs about financial ratios.`

### 3. Provide Context (So the model thinks the way you want)
* Always give background information, constraints, and assumptions.
* `Example:`
  - Context: I am preparing a Power BI workshop for beginners.  
  - Dataset: Financials sample.  
  - Audience: Business users with no technical background.

### 4. Specify the Format You Want
* Ask for the exact structure, style, or layout.
* `Example:`
  - Format: Title, 3 bullet points, A short example
  - Output: Markdown, JSON, Table format, Code blocks, Step-by-step list
  - Return the answer in a Markdown table with two columns: "Issue" and "Solution".

### 5. Add Constraints or Rules
* This forces the model to stay within boundaries.
* `Examples:`
  - Keep it under 100 words.
  - Use simple English.
  - Avoid jargon.
  - Avoid repetition.
  - Do NOT use technical formulas.
  - Provide only the final answer without explanation.

### 6. Show Examples (One of the strongest tools)
* Models learn patterns from examples. Even ONE example shapes the output dramatically.
```
Good Example
Example MCQ:
Q: Which chart type is best for showing trends over time?
A. Bar chart  
B. Line chart  
C. Pie chart  
D. Treemap  

Correct Answer: B
```
* Generate 3 similar MCQs about scatter plots.



### Prompts
```
You are a senior instructor in data analytics.

Goal:
Create a short tutorial explaining the difference between descriptive and diagnostic analytics.

Context:
- Audience: absolute beginners
- Course: Data Analytics Foundations
- Style: simple, friendly, and practical

Format:
- Title
- 2 key points each
- 1 real-world example in table format

Constraints:
- Max 150 words
- Avoid technical jargon

Example style:
“Descriptive analytics helps you understand what happened using data summaries and trends.”

Now produce the tutorial.
```

-----

## Tips and Tricks
* <|endofprompt|>
* 12yo "as if I am 12 years old"
* in simple terms; briefly; in detail; like I am an expert

