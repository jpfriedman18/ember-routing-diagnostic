# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
      The Application Router specifies the URL for every viewstate of your app.
      An Ember Route loads the model associated with a given route
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
      ember generate route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
      {{#link-to 'boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
      The first route is nested, so when the user navigates to /products/3,
      product 3 will be rendered within the products template, whereas with the
      second route, if the user goes to the same URL, the same product will be
      render but within the application template.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md

    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
      modelName.attribute
    ```
