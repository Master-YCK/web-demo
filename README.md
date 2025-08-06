# Web Demo

This is a simple Vue 3 + Vite demo project that showcases a multi-stage navigation UI using Bootstrap for styling.

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