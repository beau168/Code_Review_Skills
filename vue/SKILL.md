---
name: Vue-Review
description: Guidelines for reviewing Vue applications.
---

# Vue Code Review Guidelines

## 🏗️ Architecture
- **Composition API**: Prefer the Composition API (`<script setup>`) for better logic reuse and TypeScript support.
- **Single File Components**: Ensure SFCs are well-structured (Template, Script, Style).
- **Props & Events**: Use props for one-way data flow and `$emit` for child-to-parent communication.

## 🔄 State Management
- **Pinia/Vuex**: Use Pinia (Vue 3) or Vuex (Vue 2) for complex global state.
- **Reactive Refs**: Ensure proper usage of `ref` vs `reactive`.

## 🚀 Performance
- **v-if vs v-show**: Use `v-if` for conditional rendering and `v-show` for frequent toggling.
- **v-for Keys**: Always use unique `:key` with `v-for`.
- **Async Components**: Use `defineAsyncComponent` for lazy loading.

## 🧹 Code Quality
- **Template Logic**: Keep templates simple; use computed properties for complex logic.
- **Scoped Styles**: Use `<style scoped>` to prevent CSS leakage.
- **Naming**: Follow Vue Style Guide (e.g., PascalCase for components in templates or kebab-case).
