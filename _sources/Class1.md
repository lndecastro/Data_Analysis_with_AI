
# Class 1: Introduction to Data Analysis, AI Tools, and Careers

This class introduces the foundational concepts of data analysis and artificial intelligence, highlighting the main AI tools (ChatGPT, Claude.ai, Perplexity) that will be used throughout the course. It explores key careers in data science, essential terminology, and the principles of prompt engineering. The session also contrasts standard and AI-based approaches, emphasizing best practices for effective data analysis.

[Download the slide deck.](./DA2I_Class01_Introduction.pdf)

## Introduction to Prompt Engineering

Prompt engineering is the practice of crafting effective inputs—called prompts—to guide artificial intelligence (AI) systems, particularly large language models (LLMs), toward generating accurate, relevant, and useful outputs. It involves understanding how these models interpret language and leveraging that knowledge to frame questions, instructions, or tasks in a way that optimizes the response. Prompt engineering is essential in domains ranging from data analysis and education to content creation and software development, as it bridges the gap between human intent and machine output. As AI systems become more capable, mastering prompt engineering becomes a critical skill for anyone looking to harness the full potential of generative AI.

[Download the slide deck.](./DA2I_Class01_Prompt_Engineering_Day1.pdf)

## Hands-on activities and prompts:

### 1. Icebreaker with AI Insights
- For the mammographic_masses_nominal dataset, prompt AI as follows:
```
Here is a dataset of mammographies. Can you tell me 3 surprising insights?
```
- Which insights came from AI? Which are real? What’s your overall assessment of the result?

### 2. Analyzing Visuals with AI
- [Download the image file](./Class01_FromGoodtoBadPractices_Pictures.png), use the AI tools to analyze the quality and choice of the visuals presented in the file. You may want to try Grok.com as well!
```
I want you to act as a data analyst and analyze the attached visuals in the search for improvements or better ways of visualizing the data.
```
- How do you compare the AI analysis with the one performed by your group?

### 3. Prompt Engineering Challenge

```
You support Wildfire Risk Analysis at Montesinho Natural Park in Portugal. The superintendent needs an assessment for resource planning.
Task: Predict the fire risk level for this observation based on historical correlation with area (burned area) in the Forestfires dataset:
| X | Y | month | day | FFMC | DMC  | DC   | ISI | temp | RH  | wind | rain | area |
| 7 | 5 | mar | fri | 86.2 | 26.2 | 94.3 | 5.1 | 8.2  | 51 | 6.7  | 0 | 0 |
Step 1 - Chain-of-Thought (show your work): 
1. Compare and discuss FFMC (Fine Fuel Moisture Code): <80 = low, 80–90 = moderate, >90 = high.  
2. Compare and discuss DMC (Duff Moisture Code): <15 = low, 15–30 = moderate, >30 = high.  
3. Compare and discuss DC (Drought Code): <60 = low, 60–120 = moderate, >120 = high.
4. Compare and discuss ISI (Initial Spread Index): <3 = low, 3–6 = moderate, >6 = high.
5. Summarize weather factors: temp, RH, Wind, Rain.
6. Integrate all factors (assign appropriate weighting) to infer overall risk.
Step 2 - Analysis: Provide a paragraph discussing primary contributing factors, identifying calculated historical correlations with burned area.
Step 3 - Prediction: Based on all of the above, provide your final predicted fire risk level of the provided observation: low/medium/high.
```
