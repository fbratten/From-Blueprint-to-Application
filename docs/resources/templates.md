# Prompt Templates Reference

> Sample templates inspired by techniques from the book

---

## Basic RCT Framework

```
Role: [Who should the AI be?]
Context: [What background information is relevant?]
Task: [What specifically should the AI do?]
```

**Example:**
```
Role: You are an experienced technical writer.
Context: I'm documenting a new REST API for internal developers.
Task: Create a template for API endpoint documentation.
```

---

## Chain-of-Thought Template

```
[Your question or task]

Think through this step by step:
1. First, consider...
2. Then, analyze...
3. Finally, conclude...

Show your reasoning process.
```

---

## Few-Shot Template

```
Here are some examples:

Input: [Example 1 input]
Output: [Example 1 output]

Input: [Example 2 input]
Output: [Example 2 output]

Now, process this:
Input: [Your actual input]
Output:
```

---

## Enterprise Analysis Template

```
Role: You are a business analyst with expertise in [domain].

Context:
- Company: [Brief description]
- Current situation: [Summary]
- Constraints: [List any limitations]

Task:
Analyze the following and provide:
1. Key findings
2. Risk assessment
3. Recommended actions

Data to analyze:
[Insert data]
```

---

## Code Review Template

```
Role: You are a senior software engineer conducting a code review.

Review the following code for:
- [ ] Correctness
- [ ] Performance
- [ ] Security vulnerabilities
- [ ] Best practices
- [ ] Readability

Code:
```[language]
[Code to review]
```

Provide specific, actionable feedback.
```

---

## Output Format Control

```
Format your response as:
- **Summary**: [2-3 sentences]
- **Key Points**: [Bullet list]
- **Recommendations**: [Numbered list]
- **Next Steps**: [Action items]
```

---

> **Note:** These are simplified templates. The full book includes 50+ production-ready templates with detailed usage guides and variations.

[Get the Complete Template Library →](https://subscribepage.io/from-blueprint-to-application)

---

[← Back to Resources](../README.md)
