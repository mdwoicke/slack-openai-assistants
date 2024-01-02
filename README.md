# OpenAI Assistants - Slack Internal HR Bot Example

This repository contains the code for an internal HR bot for Slack, powered by OpenAI's API. It demonstrates how to build an AI assistant that can handle queries and perform actions within Slack. The bot can process text and image responses and includes functionality for creating tickets and calculating salaries.

## Overview

The Slack Internal HR Bot is an AI assistant that can handle various tasks within Slack. It utilizes OpenAI's Assistant API.The bot can do knowledge retrieval, call functions, run code using the code interpreter. The key point is to illustrate the capabilities of OpenAI Assistants 

## Repository Structure

- `app.py`: The main application script for handling Slack events.
- `assistants.py`: Contains the core logic for processing user queries with OpenAI and handling responses.
- `create_ticket.py`: A utility script for creating tickets in Slack.
- `create_ticket_function_definition.json`: Defines the structure for the `create_ticket` function in a format understandable by the LLM.
- `salary_calculator.py`: A script containing the `calculate_tax` and `calculate_take_home_salary` functions.
- `slack_app_manifest.yaml`: The Slack application definition manifest.
- `system_prompt.txt`: Contains the OpenAI Assistant instructions.

## Prerequisites

Before running the Slack Internal HR Bot, make sure you have the following prerequisites:

- Python 3.9
- OpenAI API key
- Slack Bot and App Tokens

## Installation

Follow these steps to install and set up the Slack Internal HR Bot:

1. Clone the repository:
    ```
    git clone https://github.com/hollaugo/slack-openai-assistants
    ```

2. Install the required packages:
    ```
    pip install openai slack_bolt
    ```
  For Search Assistant install langchain:
    ```
    pip install openai slack_bolt langchain
    ```

3. Set up the necessary environment variables:
    - `OPENAI_API_KEY`: Your OpenAI API key
    - `SLACK_BOT_TOKEN`: Your Slack bot token
    - `SLACK_APP_TOKEN`: Your Slack app token
    - `TAVILY_API_KEY`: Your Tavily api key if you are running the search assistant

## Usage

To use the Slack Internal HR Bot, follow these steps:

1. Run `app.py` to start the Slack bot:
    ```
    python app.py
    ```
- For Search assistant Run `search_assistant.py` to start:
    ```
    python search_assistant.py
    ```
2. Interact with the bot in your Slack workspace by sending messages.

## Key Features

The Slack Internal HR Bot comes with the following key features:
- Handling Slack Messages: The bot listens for messages in Slack and uses threading to handle responses asynchronously.
- Query Processing with OpenAI: User queries are processed through OpenAI's API, handling both text and image responses.
- Creating Tickets: The bot can create tickets in Slack using the `create_ticket.py` utility script.
- Calculating Salaries: The `salary_calculator.py` script provides functions to calculate tax and take-home salary.
- Uploading Files: The bot can upload in-memory files to Slack, such as images generated by OpenAI.
- Annotating File Uploads: Uploaded files can be accompanied by annotations or text responses from the assistant.

The Search Assistant is able to research topics when asked

For a detailed setup guide for Slack application, you can watch the [Slack Setup YouTube Video](https://www.youtube.com/watch?v=HQzYIWY2O2I).

## Resources 
- [Slack Bolt SDK](https://slack.dev/bolt-python/tutorial/getting-started)
- [OpenAI Assistants API Overview](https://platform.openai.com/docs/assistants/overview)
- [Langchain - Tavily Search Tool](https://python.langchain.com/docs/integrations/tools/tavily_search)
