# Chatbot for Health, Productivity, and Fitness Insights

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Data Acquisition](#data-acquisition)
- [Data Storage](#data-storage)
- [Model Architecture](#model-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository contains a chatbot designed to enhance user interaction and data analysis in the areas of **Health**, **Productivity**, and **Fitness**. The chatbot leverages **Langchain’s language models** to generate intelligent, context-aware prompts, making it easier for users to navigate and interpret data. The intuitive **Streamlit** interface allows users to interact with the chatbot, ask questions, and receive personalized app recommendations.

## Features

- **Intelligent Prompt Generation:** Uses Langchain to generate relevant prompts that guide data exploration.
- **User-Friendly Interface:** Built with Streamlit, offering a seamless experience for querying and visualizing data.
- **Targeted Recommendations:** Provides app suggestions based on user input, tailored to Health, Productivity, and Fitness categories.

## Data Acquisition

### Web Scraping

The chatbot collects app data using the **Google Play Scraper** library. It gathers information such as:

- App title
- User score
- Number of ratings
- Ads presence
- Price and whether it's free
- Install numbers
- Release date
- In-app product prices
- App icon

The data is organized into dataframes by category, enabling in-depth analysis of app performance and user feedback.

## Data Storage

### Amazon S3

All collected data is stored securely in **Amazon S3**, using the **boto3** library for authentication. This setup supports data archiving, backup, and collaboration, ensuring that the data is both secure and easily accessible.

## Model Architecture

### 1. Langchain Framework

- **Langchain** serves as the main framework, integrating the language models, data processing agents, and user interface.

### 2. Chat Model: ChatOpenAI

- The chatbot uses **ChatOpenAI** to generate responses based on user inputs, leveraging advanced NLP techniques to ensure accurate and engaging interactions.

### 3. Data Processing Agent: pandas_dataframe_agent

- Data management is handled by **pandas_dataframe_agent**, which uses the **pandas** library to clean, transform, and organize the data for optimal analysis.

### 4. Language Model: GPT-4

- **GPT-4** is the core language model, responsible for understanding user queries and generating human-like responses.

## Installation

To run this project locally, follow these steps:

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/chatbot-health-productivity-fitness.git
    cd chatbot-health-productivity-fitness
    ```

2. **Create and activate a virtual environment:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install the required packages:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Set up environment variables for AWS S3:**

    ```bash
    export AWS_ACCESS_KEY_ID=your_access_key
    export AWS_SECRET_ACCESS_KEY=your_secret_key
    ```

5. **Run the Streamlit app:**

    ```bash
    streamlit run app.py
    ```

## Usage

### Interacting with the Chatbot

1. **Select a Category:** Choose from **Health**, **Productivity**, or **Fitness** via the drop-down menu.
2. **Input Your Query:** Type in your question or data query.
3. **Request Summaries (Optional):** Specify if you need app summaries.
4. **Review Visualizations:** The chatbot will generate visualizations based on your input.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure your code follows the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
