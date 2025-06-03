# PRD: my-element Web Component

## Overview

`my-element` is a simple web component built with LitElement. It serves as a demonstration of LitElement's capabilities and best practices for web component development.

## Purpose

This component is designed to illustrate:

-   How to create a basic web component using LitElement.
-   How to define and use properties.
-   How to handle user interactions (e.g., button clicks).
-   How to use slots for custom content.
-   How to style the component using CSS and CSS Parts.

It can be used as a starting point or a reference for developers looking to build their own web components with LitElement.

## Features

-   **Customizable Greeting Message**: Displays a greeting message that can be customized via the `name` property.
-   **Click Counter**: Includes a button that, when clicked, increments a counter. The current count is displayed.
-   **Custom Content Slot**: Provides a slot where users can inject their own HTML content, allowing for flexible composition.

## Key Dependencies

-   **LitElement**: The core library used to build the component.
-   Other development dependencies (see "Build and Tooling").

## Screens/States

1.  **Initial Render (Default Properties)**:
    *   The component displays "Hello, World! Click count: 0".
    *   The button shows "Click Me!".
    *   The slot for custom content is empty by default.

2.  **With Different `name` Property**:
    *   If the `name` property is set to "Lit", the component displays "Hello, Lit! Click count: 0".

3.  **Click Counter Interaction**:
    *   When the "Click Me!" button is pressed, the `count` property increments.
    *   If the button is clicked once, the message changes to "Hello, World! Click count: 1".
    *   Subsequent clicks further increment the count.

4.  **With Custom Content**:
    *   If content is slotted into the component (e.g., `<my-element><p>Some custom content</p></my-element>`), that content will be rendered within the component's designated slot area.

## API

### Properties

-   `name`: (String, default: "World") - The name to display in the greeting message.
-   `count`: (Number, default: 0) - The current click count. This is a reactive property that updates the component's rendering when changed.

### Events

-   The component does not dispatch custom events. Standard DOM events (like `click` on the button) are available.

## Styling

-   The component is styled using standard CSS defined within its `styles` static getter.
-   It exposes a customizable CSS part named `button` which allows users to style the button from outside the component's shadow DOM.
    ```css
    my-element::part(button) {
      background-color: blue;
      color: white;
    }
    ```

## Build and Tooling

-   **TypeScript**: Used for type checking and improved JavaScript development.
-   **Rollup**: Used as the module bundler to package the component for distribution.
-   **ESLint**: For linting the codebase to maintain code quality and consistency.
-   **Prettier**: For code formatting.
-   **Eleventy (11ty)**: Used for generating the documentation site.
-   **Web Test Runner**: Used for running automated tests for the component.
