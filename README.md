### README

# Trello API Postman Collection

This Postman collection allows you to interact with the Trello API to manage boards, lists, and cards. The collection includes requests to get all boards, create a board, get a single board, create TODO and DONE lists, create a card, move the card to DONE, delete a board, and check the deletion status of a board.

## Prerequisites

- **Postman**: Make sure you have Postman installed. You can download it from [here](https://www.postman.com/downloads/).
- **Trello Account**: You need a Trello account to generate an API key and token. 

## Setup

1. **Clone or Download the Collection**: Import the Postman collection into your Postman application.

2. **Generate Trello API Key and Token**:
    - Go to Trello's [API Key page](https://trello.com/app-key).
    - Copy your API key and generate a token.

3. **Set Environment Variables in Postman**:
    - `baseUrl`: `https://api.trello.com`
    - `trelloKey`: Your Trello API key.
    - `trelloToken`: Your Trello API token.
    - `boardName`: Name of the board to be created (default is `New Board`).
    - `boardId`: ID of a specific board (default is `665b6dcc50f8bcb8eb9d65ba`).
    - `todoListId`: ID of the TODO list (leave blank initially).
    - `doneListId`: ID of the DONE list (leave blank initially).
    - `cardId`: ID of the card (leave blank initially).
    - `boardNumber`: Counter for naming boards (leave blank initially).

## Usage

1. **Get All Boards**:
    - This request retrieves all the boards associated with the user.
    - Verifies if the response status code is 200.

2. **Create Board**:
    - This request creates a new board with a name pattern `assessment <number>`.
    - Increments the board number automatically.
    - Verifies if the board is created, open, private, and if the calendar view is disabled.

3. **Get Single Board**:
    - This request retrieves the details of a specific board using `boardId`.
    - Verifies if the response status code is 200.

4. **Create TODO List**:
    - This request creates a TODO list in the specified board.
    - Verifies if the TODO list is created, open, and belongs to the correct board.

5. **Create DONE List**:
    - This request creates a DONE list in the specified board.
    - Verifies if the DONE list is created, open, and belongs to the correct board.

6. **Create Card**:
    - This request creates a card named "sign-up for trello" in the TODO list.
    - Verifies if the card is created, in the correct list and board, and has no attachments.

7. **Move Card to DONE List**:
    - This request moves the card from the TODO list to the DONE list.
    - Verifies if the card is moved to the DONE list.

8. **Delete Board**:
    - This request deletes the specified board.
    - Verifies if the response status code is 200.

9. **Get Deleted Board**:
    - This request checks the deletion status of the specified board.
    - Verifies if the response status code is 404.

## Notes

- Ensure to update the environment variables with the correct values before running the requests.
- You can customize the `boardName` variable to create boards with different names.
- The `boardNumber` variable helps in creating boards with unique names during multiple executions.

## Contributing

If you encounter any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.
