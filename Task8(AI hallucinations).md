# AI hallucinations
Imagine asking a world-class librarian for a fact, and they tell you a lie with a straight, confident face. It sounds like science fiction, but it happens every day in the world of Atcal Inteigence. While AI can solve complex equations and write poetry, it also has a habit of "hallucinating." But how, and why?

**AI hallucination is a phenomenon where, a **large language model (LLM)** often a generative AI, chatbot or computer vision tool, perceives patterns or objects that are nonexistent or imperceptible to human observers, creating outputs that are nonsensical or altogether inaccurate.
Above is the actual definition; in simple terms it is when AI gives the wrong answer confidently.

These hallucinations can occur when GenAI attempts to answer a question it can't. Instead of simply saying it doesn't know, these models generate the most likely answer. 

## Why does this happen?
LLMs are a type of generative AI that was trained on billions of pages of text and data to predict the next token (or word). They learn to mimic the style, the context, and the flow of human language rather than understanding the text they are trained on.
They also cannot respond to or give answer to a text which was not present in what the programmers had given it.

#### Some causes of AI hallucinations are :
AI hallucinations can arise from three core issues: **limitations in training data, model architecture, and the probabilistic way LLMs generate responses**
1. **Limitations in training data**
	- Hallucinations can also stem from incomplete, and **inaccurate** data sets. Inadequate or unbalanced training data can leave gaps in the model’s knowledge, especially in niche or rapidly evolving fields. AI fills the gaps using old or fictional data.
2.  **Model architecture**
	- Most modern AIs use the **Transformer architecture**, which relies on a mechanism called "Attention." In this the model may loose or forgets instructions given in the beginning 
3. **LLM's response manner**
	- The pre-training of these LLMs (GPT) involves predicting the next word. It incentivizes the models to *give a guess* about what the next word is, even when they lack information.
	- In these systems, the AI **generates each next word or token** based on a sequence of previous words (including the words it has itself previously generated during the same conversation), causing a cascade of possible hallucinations as the response grows longer. They can produce fluent but false responses if the statistical pattern resembles truth.

## Examples

- A very famous or rather infamous example is of **Google AI's (in 2024)** suggestion to add glue to keep the cheese intact on the pizza. The advice originated from an old, sarcastic Reddit post and presented as an actual solution by Google AI.

- Another one is  when in a demo of  **Google Bard**, the chatbot incorrectly claimed that the  **James Webb Space Telescope**  took the  _first-ever image of an exoplanet_ whereas the truth is that, the first exoplanet images were taken in  **2004**, long before this telescope was launched.




![Hallucination rates](https://raw.github.com/vectara/hallucination-leaderboard/2e0985929addf7fd52451854fd899161edea0aa4/img/top25_hallucination_rates_2026-03-06.png)
*This is an image of public LLM leaderboard computed using Vectara's Hallucination Evaluation Model, also known as HHEM*

![Types](https://raw.github.com/jessia-john/Marvel/194357594e56665d9a66c492832bd5949c047f94/IMG_0101.png)


## How do we prevent this?
Some ways by which we can prevent AI hallucinations include: 
1. **Using data templates :**
     Providing data template provides a predefined format to the model , increasing chances of the output aligning with the given guidelines
2. **Limiting responses :**
	One of the causes we discussed earlier was the fact that the AI models forget the constraints that were given initially. Thus to improve overall consistency 
3. **Test and refine the system continually**
	Testing your AI model before use is vital to preventing hallucinations, as is evaluating the model on an ongoing basis. These processes improve the system’s overall performance and enable users to adjust and/or retrain the model as data ages and evolves.
4. **Use high-quality training data**
Generative AI models rely on input data to complete tasks, so the quality and relevance of training datasets will dictate the model’s behavior and the quality of its outputs. In order to prevent hallucinations, ensure that AI models are trained on diverse, balanced and well-structured data.
5. Using **RAG** -- 
**Retrieval-Augmented Generation (RAG)** is a technique in where a language model first *retrieves relevant information from external data sources* and then *uses that information to generate a response*.
     - RAG adds  **retrieved facts**  to the model’s prompt
Traditional LLMs generate answers  **only from their training data**. If they don’t know something, they may invent plausible information (hallucination). RAG changes the workflow and because the answer is generated using retrieved documents, it becomes  **grounded in real data rather than guesses**.
    - Grounded generation prevents the model from inventing facts

    

## Conclusion
Thus, AI hallucinations show that even the machines we trust so much can sometimes be **extremely confident while giving incorrect answers**. 

In the fields I’d AI, researchers are constantly developing methods to reduce these errors and make AI systems more reliable. Until these solutions are fully matured, it remains our responsibility as users and developers to verify information and take steps to minimize AI hallucinations as much as possible. 

## References 
- https://cloud.google.com/use-cases/retrieval-augmented-generation
- 
- https://www.computer.org/publications/tech-news/trends/hallucinations-in-ai-models

- https://www.ibm.com/think/topics/ai-hallucinations

- https://www.sas.com/en_in/insights/articles/analytics/what-are-ai-hallucinations.html
