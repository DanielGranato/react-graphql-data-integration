# Runner Circle

A social feed app for runners and walkers, built with React, GraphQL, and Apollo Client.

## 📖 About

Runner Circle lets users log in, share their workouts ("treinos") — runs and walks — with stats like time, distance, calories, and heart rate, and browse a feed of workouts from the community, filterable by category.

This project started by consuming a REST API (via json-server) and was migrated to use GraphQL (via json-graphql-server) for data fetching, as part of Alura's "React: GraphQL para integração de dados" course.

## ✨ Features

- User login and registration
- Feed of workout posts, filterable by category (running / walking)
- Create a new workout post with time, distance, calories, heart rate, and an optional description
- Delete a workout post
- Edit profile
- Data fetching and mutations powered by GraphQL (Apollo Client)

## 🛠️ Tech Stack

- **React 19**
- **Vite**
- **Apollo Client** — GraphQL client, cache, and mutations
- **json-graphql-server** — mock GraphQL API generated from local JSON data
- **json-server** — mock REST API (used in the project's earlier, pre-GraphQL version)
- **Tailwind CSS** — utility-first styling
- **MUI** — icons and components

## 🚀 Getting Started

### Prerequisites

- Node.js
- npm

### Installation

```bash
# Clone the repository
git clone https://github.com/DanielGranato/react-graphql-data-integration.git

# Navigate into the project folder
cd react-graphql-data-integration

# Install dependencies
npm install
```

### Running locally

This project needs two processes running at the same time: the mock GraphQL server and the React app.

```bash
# Terminal 1 — start the GraphQL mock server (http://localhost:3001/graphql)
npm run server:json-graphql

# Terminal 2 — start the React app (http://localhost:5173)
npm run dev
```

A REST version of the mock server is also available via `npm run server:json-server`, kept from the project's earlier REST-based implementation.

### Other scripts

| Script | Description |
| --- | --- |
| `npm run build` | Build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
| `npm run deploy` | Build and deploy to GitHub Pages |

## 📁 Project Structure

```text
react-graphql-data-integration/
├── database/
│   ├── graphql/
│   │   ├── query/       # GraphQL queries
│   │   └── mutation/    # GraphQL mutations
│   ├── json-graphql-server.js   # mock data + GraphQL server
│   └── json-server.json         # mock data for the REST version
├── src/
│   ├── components/
│   │   ├── forms/
│   │   ├── layout/
│   │   └── ui/
│   ├── pages/            # Login, Register, Feed, NewPost, EditProfile
│   ├── main.jsx          # Apollo Client setup
│   └── App.jsx
└── README.md
```

## 🎯 Learning Objectives

This project was built to practice:

- Fetching and caching data with Apollo Client (`useQuery`)
- Creating and deleting data with GraphQL mutations (`useMutation`)
- Updating the Apollo cache after mutations (`refetchQueries`, `update`)
- Comparing a GraphQL-based data layer to a REST-based one

## 📄 License

This project is open source and available under the MIT License.
