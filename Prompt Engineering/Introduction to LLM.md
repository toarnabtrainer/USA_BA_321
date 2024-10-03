# Chapter - Important Definitions and Key Concepts

## Large Language Model (LLM) Settings

When designing and testing prompts, you typically interact with the LLM via an API. You can configure a few parameters to get different results for your prompts. Tweaking these settings are important to improve reliability and desirability of responses and it takes a bit of experimentation to figure out the proper settings for your use cases. Below are the common settings you will come across when using different LLM providers:

* **Temperature -** In short, the lower the temperature, the more deterministic the results in the sense that the highest probable next token is always picked. Increasing temperature could lead to more randomness, which encourages more diverse or creative outputs. You are essentially increasing the weights of the other possible tokens. In terms of application, you might want to use a lower temperature value for tasks like fact-based QA to encourage more factual and concise responses. For poem generation or other creative tasks, it might be beneficial to increase the temperature value.

* **Top P -** A sampling technique with temperature, called nucleus sampling, where you can control how deterministic the model is. If you are looking for exact and factual answers keep this low. If you are looking for more diverse responses, increase to a higher value. If you use Top P it means that only the tokens comprising the top_p probability mass are considered for responses, so a low top_p value selects the most confident responses. This means that a high top_p value will enable the model to look at more possible words, including less likely ones, leading to more diverse outputs.

The general recommendation is to alter temperature or Top P but not both.

* **Max Length -** You can manage the number of tokens the model generates by adjusting the max length. Specifying a max length helps you prevent long or irrelevant responses and control costs.

* **Stop Sequences -** A stop sequence is a string that stops the model from generating tokens. Specifying stop sequences is another way to control the length and structure of the model's response. For example, you can tell the model to generate lists that have no more than 10 items by adding "11" as a stop sequence.

* **Frequency Penalty -** The frequency penalty applies a penalty on the next token proportional to how many times that token already appeared in the response and prompt. The higher the frequency penalty, the less likely a word will appear again. This setting reduces the repetition of words in the model's response by giving tokens that appear more a higher penalty.

* **Presence Penalty -** The presence penalty also applies a penalty on repeated tokens but, unlike the frequency penalty, the penalty is the same for all repeated tokens. A token that appears twice and a token that appears 10 times are penalized the same. This setting prevents the model from repeating phrases too often in its response. If you want the model to generate diverse or creative text, you might want to use a higher presence penalty. Or, if you need the model to stay focused, try using a lower presence penalty.

Similar to temperature and top_p, the general recommendation is to alter the frequency or presence penalty but not both.

<hr>

## Generative Pre-trained Transformer

* Generative pre-trained transformers are a type of large language model and a prominent framework for generative artificial intelligence. They are artificial neural networks that are used in natural language processing tasks. It basically creates an output by predicting the next word in a sentence, which enables it to generate human like responses in a variety of contexts.

<hr>

## Generative AI

Generative Artificial Intelligence is artificial intelligence capable of generating text, images, videos, or other data using generative models, often in response to prompts. Generative AI models learn the patterns and structure of their input training data and then generate new data that has similar characteristics. They can be very useful in scenarios like content creation, design and problem solving.

<hr>

## Token

Tokens are the basic building blocks of input data and output format for LLMs. Each token can represent a word, part of a word, or even punctuation. Take the following sentence.

<pre>I would like to know the detailed and comprehensive meteorological
 forecast for New York this week including temperature variations,
 precipitation probabilities, and wind speeds for the upcoming week
 and all other relevant details.</pre>
 
Tokenization results in an array like this: 

<pre>["I", " would", " like", " to", " know", " the", " detailed", " and", "
 comprehensive", " meteor", "ological", " forecast", " for", " New", "
 York", " this", " week", " including", " temperature", " variations",
 ",", " precipitation", " probabilities", ",", " and", " wind", 
" speeds", " for", " the", " upcoming", " week", " and", " all", 
" other", " relevant", " details"]</pre>

Tokens are crucial because they transform complex, variable-length text into a uniform format that the model can understand and process. Each token is analyzed in context so the model learns not just the token, but its relationship with others. The model generates output by predicting the next token in a sequence, based on the patterns and relationships it has learned.

<hr>

## Artificial General Intelligence (AGI)

Artificial general intelligence is a type of artificial intelligence that can perform as well or better than humans on a wide range of cognitive tasks. This is in contrast to narrow AI, which is designed for specific tasks. AGI is considered one of various definitions of strong AI.

<hr>

## AI alignment

* In the field of artificial intelligence, AI alignment research aims to steer AI systems toward a person's or group's intended goals, preferences, and ethical principles. An AI system is considered aligned if it advances its intended objectives.

<hr>

## Reinforccement Learning from Human Feedback

In machine learning, reinforcement learning from human feedback is a technique to align an intelligent agent to human preferences. In classical reinforcement learning, the goal of such an agent is to learn a function that guides its behavior called a policy. So it's actually a way of aligning AI models to our values. This feedback helps the AI system learn to make better decisions and adapt its behavior to better align with human values and goals. 

ChatGPT and GPT4 are examples of AI models that were trained using this technique so we can say it's a method that's used to achieve a better alignment of an AI.

<hr>

## AI Fine-tuning

Fine-tuning is the process of taking a pretrained machine learning model and further training it on a smaller, targeted data set. The aim of fine-tuning is to maintain the original capabilities of a pretrained model while adapting it to suit more specialized use cases.

AI fine tuning is a technique where a pre-trained model is further trained on a smaller set of data specific to a particular domain. This tuning will improve the model's performance on the respective topic. It's like taking a person with standard education into a specialized course for a particular domain. It's like taking a person with standard education into a specialized course for a particular domain.

<hr>

## chatGPT and GPT4

ChatGPT is a chatbot developed by OpenAI and launched on November 30, 2022. Based on large language models, it enables users to refine and steer a conversation towards a desired length, format, style, level of detail, and language. 

Generative Pre-trained Transformer 4 is a multimodal large language model created by OpenAI, and the fourth in its series of GPT foundation models. It was launched on March 14, 2023, and made publicly available via the paid chatbot product ChatGPT Plus, via OpenAI's API, and via the free chatbot Microsoft Copilot.

The news was rolled out by OpenAI on Twitter that “ChatGPT can now browse the internet to provide you with current and authoritative information, complete with direct links to sources. It is no longer limited to data before September 2021.”

<hr>
