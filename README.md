# GraphQL Game Review API

This is a GraphQL API for managing game reviews, authors, and games. It allows you to perform various queries and mutations to interact with your gaming data.

**Table of Contents**

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Running the API](#running-the-api)
- [Using the API](#using-the-api)
  - [Queries](#queries)
  - [Mutations](#mutations)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

These instructions will help you set up and run the GraphQL Game Review API on your local system.

### Prerequisites

Before you begin, ensure you have met the following requirements:

- Node.js and npm installed on your machine.
- Git for version control.

### Installation

1. Clone this repository to your local machine:

   ```bash
   git clone <repository-url>
   Navigate to the project directory:
   ```

   ```bash
   cd graphql-game-review-api
   ```

2. Install project dependencies:

   ```bash
   npm install
   ```

### Running the API

1. Start the GraphQL server:

   ```bash
   npm start
   ```

2. The GraphQL server should now be running locally on http://localhost:4000/graphql.

### GraphQL Playground

    You can use the GraphQL Playground to interact with the API. Open your web browser and navigate to http://localhost:4000/graphql to access the Playground.

## Using the API

### Queries

- To retrieve a list of games, use the following query:

```graphql
{
  games {
    id
    title
    platform
  }
}
```

- List of Reviews
  To fetch reviews, use:

````graphql
{
    reviews {
        id
        rating
        content
    }
}

List of Authors
To get list of authors
```graphql
{
    authors {
        id
        name
        verified
    }
}
````

### Mutations

Create a New Game

```graphql
mutation {
  createGame(
    input: { title: "Game Title", platform: ["Platform 1", "Platform 2"] }
  ) {
    id
    title
    platform
  }
}
```

Post a Review

```graphql
mutation {
  createReview(input: { rating: 4, content: "This game is amazing!" }) {
    id
    rating
    content
  }
}
```

Add a New Author

```graphql
mutation {
  createAuthor(input: { name: "John Doe", verified: true }) {
    id
    name
    verified
  }
}
```

### Contributing

Feel free to contribute to this project by opening issues or submitting pull requests.

### License

This project is licensed under the MIT License - see the LICENSE file for details.
