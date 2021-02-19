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
Collecting the data is also simple. The categorical container wrapped in a form makes it easy to grab your data on the server as each user input will genearate a hidden input field equal to the value of the input. It's recommended to include a nameAttribute such as *requestBody[category]* to easily grab all the rendered strings from the request body. No form is fine too. An async approach is easy too as each input field value sits right under the *data-added* class span. Some simple JS will do the trick:

```javascript
document.querySelectorAll('.data-add > input');
```

