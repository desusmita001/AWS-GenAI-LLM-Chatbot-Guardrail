# AWS-GenAI-LLM-Chatbot-Guardrail
Implementing Responsible AI Controls using Amazon Bedrock to detect and block Financial Advice queries in an LLM Chatbot.

---

## Project Overview
Large Language Models (LLMs) can unintentionally generate regulated or sensitive content such as financial advice.  
This project demonstrates how to implement topic-based guardrails using Amazon Bedrock to:

- Detect financial advice queries
- Block unsafe responses
- Return a compliant denial message
- Log policy intervention in trace output
- Provide topic-level enforcement visibility

> Built using a **personal AWS account** for demonstration purposes.

---

## Architecture Overview
User Prompt → Bedrock LLM → Guardrail Policy → Topic Detection → Response Filter → Safe Output


The guardrail intercepts the model output before final response delivery.

---

## Guardrail Demonstration

### Financial Advice Query Automatically Blocked
**Input Prompt:**
Give me financial advice.

**Output Response:**
Sorry, the model cannot answer this question.

![Slide 1](https://github.com/desusmita001/AWS-GenAI-LLM-Chatbot-Guardrail/blob/main/screenshots/1.png)

### Real-Time Guardrail Intervention Triggered
The system logs a policy violation and displays a warning indicator showing intervention.

![Slide 2](https://github.com/desusmita001/AWS-GenAI-LLM-Chatbot-Guardrail/blob/main/screenshots/2.png)

### Topic-Level Detection Trace
Under denied topics:

- FinancialAdvice: Blocked  
- Detected: True  

This confirms the guardrail successfully classified and enforced the restriction.

![Slide 3](https://github.com/desusmita001/AWS-GenAI-LLM-Chatbot-Guardrail/blob/main/screenshots/3.png)

### Additional Screenshot
![Slide 4](https://github.com/desusmita001/AWS-GenAI-LLM-Chatbot-Guardrail/blob/main/screenshots/4.png)

---

## Key Concepts Demonstrated

- Responsible AI implementation  
- AI governance and compliance controls  
- Topic-based content filtering  
- Risk mitigation in GenAI systems  
- Trace-level transparency for auditing  
- Safe conversational AI design