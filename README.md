# Web Demo

> A Vue 3 + Vite demo project showcasing multi-stage navigation UI with Bootstrap 5 for responsive design

This is a simple Vue 3 + Vite demo project that showcases a multi-stage navigation UI using Bootstrap for styling.

## 📋 About

This repository demonstrates modern web development practices using Vue 3's Composition API, Vite's lightning-fast build tooling, and Bootstrap 5's responsive components. The project features a multi-stage navigation component that allows users to step through different stages with visual feedback for active and completed stages.

### Topics

`vue` `vue3` `vite` `bootstrap` `bootstrap5` `frontend` `web-demo` `ui-components` `navigation` `responsive-design`

## Features

- Vue 3 with Composition API
- Vite for fast development and build
- Bootstrap 5 for responsive UI
- Multi-stage navigation component (`StateView`)

## Project Structure

```
├── src/
│   ├── App.vue
│   ├── main.js
│   └── components/
│       └── stateView.vue
├── public/
│   └── vite.svg
├── index.html
├── package.json
├── vite.config.js
```

## Getting Started

### Prerequisites

- Node.js (v16 or higher recommended)
- npm

### Install dependencies

```sh
npm install
```

### Run the development server

```sh
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser to view the app.

### Build for production

```sh
npm run build
```

### Preview the production build

```sh
npm run preview
```

## Usage

The main component is [`StateView`](src/components/stateView.vue), which displays a navigation bar with multiple stages. Use the "Previous" and "Next" buttons to navigate between stages. The active and completed stages are visually indicated.

## License

This project is for demonstration purposes.