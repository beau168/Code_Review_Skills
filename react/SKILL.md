---
name: React-Review
description: Guidelines for reviewing React applications.
---

# React Code Review Guidelines

## 🏗️ Architecture
- **Functional Components**: Prefer functional components and Hooks over class components.
- **Custom Hooks**: Extract logic into custom hooks for reusability across components.
- **Prop Drilling**: Avoid deep prop drilling; use Context API or state management libraries (Redux, Zustand) for global state.

## 🔄 Hooks & Lifecycle
- **Dependency Arrays**: ensure `useEffect`, `useMemo`, and `useCallback` have correct dependency arrays.
- **Rules of Hooks**: Verify hooks are called at the top level and not inside loops or conditions.

## 🚀 Performance
- **Memoization**: Use `React.memo`, `useMemo`, and `useCallback` judiciously to avoid unnecessary re-renders.
- **Code Splitting**: Use `React.lazy` and `Suspense` for route-based code splitting.

## 🧹 Code Quality
- **JSX Best Practices**: Keep JSX clean; avoid complex logic inside return statements.
- **PropTypes/TypeScript**: Use TypeScript (preferred) or PropTypes for type checking.
- **Naming**: Use PascalCase for components and camelCase for functions/variables.
