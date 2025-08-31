# Gemini Code Assistant Context

## Project Overview

`fighting-design` is a Vue.js component library that provides over 60 reusable components for building interactive user interfaces. The library is built with Vite, written in TypeScript, and has no third-party dependencies, making it lightweight and fast. It supports both full and on-demand import, providing flexibility for different project needs.

The project is structured as a monorepo using pnpm workspaces, with the main packages being:

-   `packages/fighting-design`: The core component library.
-   `docs`: The documentation site, built with VitePress.
-   `start`: A project for quick starting.

## Building and Running

The following commands are essential for working with the project:

-   **Installation:**
    ```bash
    pnpm install
    ```
-   **Running the documentation site:**
    ```bash
    pnpm dev:docs
    ```
-   **Building the library:**
    ```bash
    pnpm build
    ```
-   **Running tests:**
    ```bash
    pnpm test
    ```
-   **Linting and formatting:**
    ```bash
    pnpm lint
    pnpm format
    ```

## Development Conventions

The project follows a set of development conventions to ensure code quality and consistency:

-   **Package Manager:** `pnpm` is used for package management.
-   **Monorepo:** The project is organized as a monorepo using pnpm workspaces.
-   **Build Tool:** Vite is used for building the library and documentation site.
-   **Component Development:** Components are written in TypeScript and Vue.
-   **Styling:** The project uses Sass for styling.
-   **Linting and Formatting:** ESLint and Prettier are used for code linting and formatting.
-   **Commit Messages:** Commit messages are standardized using Commitizen and Commitlint.
-   **Documentation:** The documentation is generated using VitePress.
