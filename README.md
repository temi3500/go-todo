# Todo CLI Application

This is a simple Todo Command Line Interface (CLI) application written in Go. It allows users to manage their tasks efficiently by adding, editing, toggling, deleting, and listing todos directly from the terminal.

## Features

- **Add a Todo**: Add a new todo with a title.
- **Edit a Todo**: Edit an existing todo by specifying its index and the new title.
- **Delete a Todo**: Remove a todo by its index.
- **Toggle Completion**: Mark a todo as completed or incomplete by toggling its status.
- **List Todos**: Display a formatted list of all todos with details like title, completion status, creation date, and completion date.

## Prerequisites

- [Go](https://golang.org/dl/) (version 1.16 or higher)

## Installation

1. Clone the repository:
   ```bash
   git clone
   cd todo
   ```
2. Build the application:
   ```bash
   go build -o todo
   ```

## Usage

Run the application using the `go run` command or the compiled binary. Below are the supported commands:

### List Todos
```bash
./todo --list
```
Displays all todos in a formatted table.

### Add a Todo
```bash
./todo -add "<title>"
```
Adds a new todo with the specified title.

Example:
```bash
./todo -add "Go for a walk"
```

### Edit a Todo
```bash
./todo -edit <index>:<new_title>
```
Edits the todo at the specified index and updates the title.

Example:
```bash
./todo -edit 0:"Read a book"
```

### Toggle a Todo
```bash
./todo -toggle <index>
```
Toggles the completion status of the todo at the specified index.

Example:
```bash
./todo -toggle 0
```

### Delete a Todo
```bash
./todo -del <index>
```
Deletes the todo at the specified index.

Example:
```bash
./todo -del 0
```

## Example Usage

Adding a todo:
```bash
./todo -add "Go for a walk"
```

Listing todos:
```bash
./todo --list
┌───┬───────────────┬───────────┬───────────────────────────────┬──────────────┐
│ # │     Title     │ Completed │          Created At           │ Completed At │
├───┼───────────────┼───────────┼───────────────────────────────┼──────────────┤
│ 0 │ Go for a walk │ ❌        │ Mon, 27 Jan 2025 21:05:03 PKT │              │
└───┴───────────────┴───────────┴───────────────────────────────┴──────────────┘
```

Toggling a todo:
```bash
./todo -toggle 0
```

Deleting a todo:
```bash
./todo -del 0
```

## Error Handling

- Invalid commands or arguments will display an appropriate error message.
- For editing, the format must be `index:new_title`, e.g., `0:New Title`. An error will be shown if the format is incorrect.






