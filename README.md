# Conversational AI with Memory using R

This project implements a conversational AI chatbot using Rasa that retains context across conversation turns through session-based memory. The chatbot is capable of greeting users, remembering their names, and responding to goodbye intents.

## Project Structure

```
conversational_ai_with_memory/
├── actions/
│   └── actions.py          # Custom actions for the chatbot
├── data/
│   ├── nlu.yml             # NLU training data
│   └── rules.yml           # Rules for conversation management
├── config.yml               # Configuration for the Rasa pipeline and policies
├── domain.yml               # Domain definition including intents, entities, and responses
├── endpoints.yml            # Endpoints for the Rasa server
├── credentials.yml          # Credentials for connecting to channels
└── README.md                # Project documentation
```

## Setup Instructions

1. **Install Dependencies**:
   Ensure you have Python installed, then install the required packages:
   ```
   pip install rasa
   pip install rasa-sdk
   ```

2. **Train the Model**:
   Navigate to the project directory and run:
   ```
   rasa train
   ```

3. **Start the Action Server**:
   In a new terminal, start the action server:
   ```
   rasa run actions
   ```

4. **Start the Chatbot**:
   In another terminal, run the chatbot:
   ```
   rasa shell
   ```

## Usage Guidelines

- The chatbot can greet users and ask for their names.
- It remembers the user's name throughout the session and can respond to queries about it.
- The chatbot can say goodbye when the user indicates they want to end the conversation.

## Additional Information

For more details on Rasa and its capabilities, please refer to the [Rasa documentation](https://rasa.com/docs/rasa).
