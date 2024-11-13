# Practice: Mongoose Methods


## Iteration 0: Initial Setup

- Fork
- Clone
- Open with VS Code
- Run with `npm run dev`

Note: if you're already running an app on port 3000, change the variable `PORT` (at the beginning of `app.js`) and run again with `npm run dev`.



## Iteration 1: Implement an endpoint to get a list of pizzas from the DB

- In app.js, create a new route `GET /pizzas`

- Inside this route, you can use the mongoose method "find()". Example:

  ```js
  Pizza.find()
    .then()
    .catch()
  ```

- Test your route:
    - You will need to send a GET request to "/pizzas"



## Iteration 2: Implement an endpoint to get one pizza from the DB

- In app.js, create a new route `GET /pizzas/:pizzaId`

- Inside this route,
    - Get the pizza id from `req.params`
    - To get a document from the DB, use the mongoose method "findById()". Example:

        ```js
        Pizza.findById()
            .then()
            .catch()
        ```

- Test your route:
    - You will need to send a GET request to "/pizzas/abc" (where `abc` is a valid id)
    - Note: to get a valid id, you can use the endpoint you created in the previous iteration (ie. when you get a list of pizzas, you'll be able to see their id's)



## Bonus: filter pizzas by max price

Modify the route `GET /pizzas`, so that it allows you to filter pizzas by max price.

Examples:
- `http://localhost:3000/pizzas` should return an array with all the pizzas in our DB.
- `http://localhost:3000/pizzas?max_price=12` should return an array with all pizzas with a max price of 12.
- `http://localhost:3000/pizzas?max_price=15` should return an array with all pizzas with a max price of 15.

