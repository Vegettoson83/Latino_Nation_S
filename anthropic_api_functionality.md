# Anthropic API Functionality

This document breaks down the functionality of the Anthropic API, categorizing its features and describing their purpose based on the official documentation.

## Core Functionality

The core of the Anthropic API revolves around the **Messages API**, which allows for generating conversational responses. This can be used for single-turn or multi-turn conversations.

- **Message Creation**: The primary function of the API is to create messages. This is done by sending a series of messages with roles (`user` and `assistant`) to the model, which then generates the next message in the conversation.

## Advanced Features

### Batches

The Batches API allows for processing large numbers of messages asynchronously. This is useful for large-scale applications that don't require real-time responses.

### Models

The Models API provides information about the available models, including their capabilities and pricing.

## Tools

The Anthropic API can be extended with tools, which allow the model to interact with external systems. There are two types of tools:

- **Client Tools**: These are tools that you define and implement on your own systems. When the model determines that a client tool is needed, it will return a `tool_use` stop reason, and you will be responsible for executing the tool and returning the results to the model.
- **Server Tools**: These are tools that are hosted by Anthropic. When the model uses a server tool, the tool is executed on Anthropic's servers, and the results are automatically incorporated into the model's response.

### Available Server Tools

- **Web Search**: Allows the model to search the web to answer questions about recent events or to find information that is not in its training data.
- **Web Fetch**: Allows the model to fetch the content of a URL.

### Custom Tools

You can also create your own custom tools to extend the functionality of the API. This is done by providing a tool definition in the API request, which includes the tool's name, description, and input schema.
