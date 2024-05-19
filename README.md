# HomeMatch

**HomeMatch** is a personalized real-estate agent using GenAI technologies. It generates real-estate listings (including images), it interviews users about their preferences and identifies the best matches in the real estate database. Once the agent identifies those matches, it updates the listings to *personalize* them by emphasizing the most appealing features to the users.

## Gen AI features

**HomeMatch** relies on LangChain for its GenAI capabilities. LangChain is an abstraction layer which allows us to build GenAI pipelines using different LLM models. So, it's easier to switch LLMs without having to rewrite our code.

HomeMatch leverages GenAI models to perform the following tasks:

* Generate real estate listings.
* Generate images for those real estate listings using a diffusion model.
* Summarize the user preferences.
* Personalize of the listings based on the user preferences.

## Multimodal Search

In this project, we also explore multi-modal searches. We use Chroma vector database to encode real estate listings and images. Using the multi-modal search, we can then search the best match properties using a textual or image search.

## Chatbot experience

In the first part of the project, we hard-coded some questions and answers to capture the user's preferences. However, in a real-case scenario, it's better to use a chatbot interface. So, we built a chat bot interface in this project too.

## Project set up

To run this project, clone the repo using the following command:

The project relies on an environment variable to get access to the openAI environment. Update the .env file with your API key as follows:

## Project Files

This project is composed of a few files and folders:

  1. **HomeMatch.ipynb** - this is Jupyter Notebook for the main project file which outlines the project step by step.
  2. **RealEstateGeneration.ipynb** - this is the Jupyter Notebook which is used to generate images based on the real estate descriptions.
  3. **listings.json**: JSON file with the generated real-estate listings. We save them as a file so we don't need to regenerate them all the time. It's also useful to generate the images from this file.
  4. An **images/generated** folder which includes 10 images generated based on the real-estate descriptions.
  5. An **images/search** folder which includes images that are used to test the multi-modal search.
  6. **requirements.txt** file includes all the packages that need to be installed to run this project.