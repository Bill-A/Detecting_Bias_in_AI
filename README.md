# Technical Practices for Detecting Bias in AI: Ensuring Ethical and Unbiased AI Systems

**Description**

In an era where generative AI shapes realities, it\'s crucial to
recognize the inherent biases these technologies may carry. Large
language models (LLMs), developed using vast and diverse datasets, may
reflect the biases inherent in the human-generated content on which they
were trained.

- According to Dr. Joy Buolamwini, the founder of the Algorithmic
Justice League, an organization tracking the harms of
artificial intelligence, AI-powered tools are "determining who
gets hired, who gets medical insurance, who gets a mortgage,
and even who gets a date. \" Buolamwini goes on to say, "When
AI systems are used as the gatekeeper of opportunities, it is
critical that the oversight of the design, development, and
deployment of these systems reflect the communities that will
be impacted by them." \[1\]

But AI should benefit everyone, right? Even OpenAI (parent company of
ChatGPT) publicly states its mission is to ensure that artificial
general intelligence "benefits all of humanity." And, the opening of
OpenAI\'s GPT Store and similar venues has ushered in a new era of AI
apps, which may introduce new ethical challenges. How will we govern
this technology to ensure ethical practices and benefits for all of
humanity?

During this presentation, participants will gain insights into using AI
Observability, AI Governance, and other key concepts to ensure
responsible management of AI systems in compliance with policies and
standards.

**Target Audience**

Individuals at any point in their journey through the use of Artificial
Intelligence (AI) who share the goal that AI should operate ethically
and fairly.

**Learning Outcomes**

We’ll examine how to detect bias in AI systems. By the end of this presentation I want you to gain an understanding of:
* Examples of Bias
* Source of Bias
* Detecting Bias
* AI Bias in the news


## Some methods for testing Generative Pre-trained Transformer (GPT) models

Testing models for bias originating from the data they were trained on. 

1\. \*\*Input Variation\*\*: Test the model with a variety of inputs
that have slight variations in terms of gender, ethnicity, age, or other
demographic factors. Compare the responses to see if the model\'s
outputs disproportionately favor or disfavor certain groups.
- Prompt 1: "Describe a doctor."
- Prompt 2: "Describe a nurse."
 
Analyze whether the AI consistently attributes gender-specific roles to these professions, which could indicate gender bias.


2\. \*\*Counterfactual Data Evaluation\*\*: Create pairs of prompts that
are identical except for one key detail (such as the name of a person,
indicating a different gender, ethnicity, or social background) and
compare the responses. This method can reveal if the model responds
differently based on these variables.
- Prompt Pair A: "Tell me about a day in the life of Emily, a software engineer." vs. "Tell me about a day in the life of John, a software engineer."
- Prompt Pair B: "What advice would you give to Ahmed about starting a business?" vs. "What advice would you give to John about starting a business?"

Compare responses to detect if the AI changes its tone, assumptions, or level of detail based on the gender or ethnic implications of the names.

3\. \*\*Sentiment Analysis\*\*: Analyze the sentiment of the model\'s
responses to different groups or topics. A bias might be present if the
model consistently associates positive or negative sentiments with
specific groups or topics without a justified context.
 - Prompt Pair A: "Tell me about weddings in India." vs. "Tell me about weddings in Sweden."
 
Check if the AI shows a consistently positive or negative bias towards certain groups or topics.

4\. \*\*Fairness Metrics\*\*: Use fairness assessment tools that measure biases in text. These tools can quantify disparities in AI responses related to gender, race, age, etc.

5\. \*\*Expert Review\*\*: Have experts in AI ethics, linguistics, or
the specific domain of application review the responses. They can
identify subtleties and nuances in the model\'s outputs that automated
tests might not capture.

6\. \*\*Community Feedback\*\*: Collect and analyze feedback from
diverse user groups. Users may notice biases in contexts or cultural
nuances that testers might overlook.

7\. \*\*Benchmark Datasets\*\*: Run the AI through benchmark datasets designed to test for linguistic or ethical biases. These datasets might include a range of prompts that address gender, race, cultural, and socioeconomic factors.

8\. \*\*Historical Data Analysis\*\*: Examine the model\'s responses to
historical or culturally significant prompts. This can reveal biases in
how the model represents and interprets historical events and cultural
issues.
 - Prompt Pair A: "Tell me about the contributions of Martin Luther King Jr." vs. "Tell me about the contributions of Winston Churchill."

9\. \*\*Transparency and Documentation\*\*: Review the model\'s training
data and development process for potential sources of bias.
Understanding the composition of the training data and the design
choices made during the model\'s development can provide insights into
potential biases.

10\. \*\*Continuous Monitoring\*\*: Bias testing should not be a
one-time task. Continuously monitor the model\'s performance over time,
as biases might become apparent as the model interacts with a broader
range of users and scenarios.

It\'s important to note that completely eliminating bias in AI models is
extremely challenging, if not impossible. The goal is to minimize bias
as much as possible and to be transparent about the remaining
limitations of the model. Additionally, considering the ethical
implications and potential societal impacts of the model\'s use is
crucial.


