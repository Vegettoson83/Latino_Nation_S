# Anthropic API Structure

This document outlines the structure of the Anthropic API, including endpoints and HTTP methods, based on the official documentation.

## Base URL

`https://api.anthropic.com/v1`

## Authentication

Authentication is handled via an `x-api-key` header.

## Endpoints

### Messages

- **POST /messages**: Creates a new message.

### Batches

- **POST /batches**: Create and submit a batch request.
- **GET /batches/{batch_id}**: Retrieve a batch request.
- **POST /batches/{batch_id}/cancel**: Cancel a batch request.
- **GET /batches/{batch_id}/results**: Retrieve the results of a batch request.
- **DELETE /batches/{batch_id}**: Delete a batch request.
- **GET /batches**: List batch requests.

### Models

- **GET /models**: Lists all available models.
- **GET /models/{model_id}**: Retrieves a specific model.

### Text Completions (Legacy)

- **POST /complete**: Creates a new text completion.
