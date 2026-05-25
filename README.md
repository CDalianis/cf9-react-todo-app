# CF9 React Todo App

A clean and responsive task management application built with React, TypeScript, Vite, and Tailwind CSS. The app is designed around a simple productivity workflow with persistent local storage, inline editing, and a small reusable component architecture.

## Overview

This project is a modern front-end todo application that demonstrates:

- fast local development with Vite
- type-safe UI development with TypeScript
- reusable React components
- custom state management with a dedicated hook
- persistent browser storage with `localStorage`

## Features

- Add new tasks from a simple input form
- Mark tasks as completed or active
- Edit tasks inline directly inside the list
- Delete individual tasks
- Clear all tasks with one action
- View live statistics for total, active, and completed items
- Keep todos saved between page refreshes using `localStorage`
- Use a responsive layout with shared header and footer components

## Tech Stack

- React 19
- TypeScript
- Vite
- Tailwind CSS 4
- Lucide React
- ESLint

## Getting Started

### Prerequisites

- Node.js 20 or newer recommended
- npm

### Installation

```bash
npm install
```

### Start the Development Server

```bash
npm run dev
```

After the server starts, open the local URL shown in the terminal, typically `http://localhost:5173`.

## Available Scripts

```bash
npm run dev
```

Starts the Vite development server with hot module replacement.

```bash
npm run build
```

Builds the application for production.

```bash
npm run preview
```

Previews the production build locally.

```bash
npm run lint
```

Runs ESLint across the codebase.

## Project Structure

```text
src/
  features/
    todo/
      hooks/
      TodoApp.tsx
      TodoForm.tsx
      TodoList.tsx
      TodoStats.tsx
      types.ts
  shared/
    layout/
    ui/
    types.ts
  App.tsx
  index.css
  main.tsx
```

## Architecture

The core todo logic lives in the `useTodos` hook. It is responsible for:

- creating tasks
- editing tasks
- toggling completion state
- deleting tasks
- clearing the full list
- synchronizing state to browser storage

The UI is split into focused components:

- `TodoForm` handles input and task creation
- `TodoList` renders tasks and inline edit actions
- `TodoStats` displays live counters
- `Layout` provides the shared page structure

## Data Persistence

Todos are stored in the browser under the `todos` local storage key. This allows tasks to remain available after a page refresh on the same browser and device.

## Production Build

To generate an optimized build:

```bash
npm run build
```

The compiled files are output to the `dist/` directory.

## Future Improvements

- add filtering for all, active, and completed tasks
- support priorities or due dates
- add drag-and-drop task ordering
- improve accessibility and keyboard support
- add automated tests for the todo workflow

## License

This project is intended for educational or portfolio use unless a separate license is added to the repository.
