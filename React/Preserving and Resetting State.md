# Preserving and Resetting State

Key points

- React uses a tree structure to manage and model the UI.
- State in React is tied to the position of components in the UI tree.
- Each component on the screen has fully isolated state.
- **React preserves the state of a component as long as it is rendered at the same position in the UI tree.**
- **React preserves the component if the key is same**
- Key is not global. It's scoped by the position or parent element.
- When a component is removed or replaced with a different component at the same position, React discards its state.
- The position in the UI tree, not the JSX markup, determines whether the state is preserved or reset.
- Swapping components of different types at the same position results in the state being reset.

Old:Reconciliation
https://legacy.reactjs.org/docs/reconciliation.html
New: Preserving and Resetting State
https://react.dev/learn/preserving-and-resetting-state
