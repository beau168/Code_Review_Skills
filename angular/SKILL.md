---
name: Angular-Review
description: Guidelines for reviewing Angular applications.
---

# Angular Code Review Guidelines

## 🏗️ Architecture
- **Component Decomposition**: Ensure components are not too large. Promote reusability.
- **Smart vs. Dumb Components**: Use the container/presentational pattern where appropriate.
- **Module Organization**: Check for proper use of Feature Modules, Shared Modules, and Core Modules.

## 🔄 State Management & RxJS
- **RxJS Best Practices**: Use the `async` pipe to avoid manual subscriptions and potential memory leaks.
- **Unsubscribing**: If manual subscription is necessary, ensure proper unsubscription (e.g., `takeUntil`, `SubSink`).
- **Immutability**: Ensure state updates are done immutably.

## 🚀 Performance
- **Change Detection**: Use `OnPush` change detection strategy where possible.
- **Lazy Loading**: Ensure feature modules are lazy-loaded to reduce initial bundle size.
- **TrackBy**: Use `trackBy` function with `*ngFor` for large lists.

## 🧹 Code Quality
- **Standard Style**: Follow the official Angular Style Guide (e.g., prefixing components, file naming).
- **Templates**: Keep logic out of templates; move it to the component class.
- **Strict Typing**: Leverage TypeScript's strict mode and avoid using `any`.
