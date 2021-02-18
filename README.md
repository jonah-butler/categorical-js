# Categorical-JS

## Use Case
Categorical is a provided class to handle a type of text input where the user must provide a series of strings, such as a tag input for a blog or a tag input for adding query limiters to a search. Categorical handles the UI interactions, builds the input fields with the user input value and performs client side validation on each entered string. 

## In Action
https://jonah-butler.github.io/categorical-js/

## Accepted Characters
* [a-zA-Z]
* [0-9]
* [~`!@#$%^&*()_+=\][|}{';":/.,?>< ]

## Initializing
It's easy to initialize Categorical.

```html
<div class="tag-input-container">
  <div class="headline">Add Category</div>
  <div id="spanContainer"></div>
  <input class="tag-input-component" type="text">
</div>
```

```javascript
Categorical(mainTextInput, spanContainer, nameAttribute);
```

```javascript
const categorical = new Categorical(document.querySelector('.tag-input-component'), document.querySelector('#spanContainer'), inputName);
categorical.init();
```
## Sending Data to a Server
Collecting the data is also simple. It's recommended to include an inputName such as *requestBody[category]* to easily grab all the rendered strings from a request.
