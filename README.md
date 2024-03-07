### Text To SQL LLM App Readme
## Introduction
This project is a Text To SQL LLM (Large Language Model) App integrated with Google Gemini Pro for generating SQL queries based on natural language input. It also enables querying SQL databases directly using the generated SQL commands.

## Code Overview

## Import Libraries: 

The code begins by importing necessary libraries such as dotenv, streamlit, os, sqlite3, and google.generativeai.

## Configure API Key: 

It configures the API key for accessing the Google Gemini Pro model using the genai.configure() function.

## Define Functions:

get_gemini_response: This function takes a question and a prompt as input, uses the Gemini Pro model to generate a response based on the provided question and prompt, and returns the generated response.
read_sql_query: This function executes an SQL query on a specified database and returns the result rows.

## Define Prompt: 

A prompt is defined as a multi-line string. This prompt provides instructions and examples for converting English questions to SQL queries.

## Streamlit App Setup:

Streamlit page configuration is set using st.set_page_config.
A header is added to the Streamlit app using st.header.

## User Interaction:

A text input field is provided to allow users to input their questions.
A submit button enables users to submit their questions.

## Response Processing:

When the submit button is clicked, the input question is passed to the get_gemini_response function along with the defined prompt.
The response generated by the Gemini Pro model is then used to execute an SQL query using the read_sql_query function.

## Display Output:

The response from the SQL query is displayed as a subheader using st.subheader.