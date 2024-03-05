# jQuery-3.7.1-Cheatsheet
[jQuery API Documentation](https://api.jquery.com/).

---

# jQuery 3.7.1 Features Guide
A Interactive Cheatsheet: https://oscarotero.com/jquery/

## Setup

### 1. **Getting Started with jQuery:**

- **Include jQuery:**
  Make sure to include jQuery in your HTML file. You can download it from the [official website](https://jquery.com/download/) or use a CDN.

  - Uncompressed
    ```html
    <script src="https://code.jquery.com/jquery-3.7.1.js" integrity="sha256-eKhayi8LEQwp4NKxN+CfCh+3qOVUtJn3QNZ0TciWLP4=" crossorigin="anonymous"></script>
    ```
  - Compressed
    ```html
    <script src="https://code.jquery.com/jquery-3.7.1.min.js" integrity="sha256-/JqT3SQfawRcv/BIHPThkBvs0OEvtFFmqPF/lYI/Cxo=" crossorigin="anonymous"></script>
    ```
## Core Features


### 1. **Selecting Elements:**

- **Basic Selectors:**
  jQuery uses CSS selectors to select elements. Here are some examples:

  ```javascript
  // Select all button elements
  var buttons = $("button"); 

  // Select by tag name
  $('p')

  // Select by class
  $('.myClass')

  // Select by ID
  $('#myId')
  ```

### 2. **DOM Manipulation:**

- **Adding and Removing Elements:**
  ```javascript
  // Append content to an element
  $('#myDiv').append('<p>New content</p>');

  // Remove an element
  $('.toBeRemoved').remove();

  // Modify the html contents
  $("button.continue").html("Next Step...");

  ```

- **Modifying Attributes:**
  ```javascript
  // Change attribute value
  $('#myImage').attr('src', 'newImage.jpg');

  // Remove attribute
  $('#myLink').removeAttr('target');
  ```

### 3. **Each Method**
 - **Iterate over an array or object.**
    ```javascript
    var arr = [1, 2, 3, 4, 5];
    $.each(arr, function(index, value) {
      console.log("Index: " + index + ", Value: " + value);
    });
    ```

### 4. **Grep Method**
- **Filter elements from an array.**
  ```javascript
  var numbers = [1, 2, 3, 4, 5];
  var evens = $.grep(numbers, function(element) {
    return element % 2 === 0;
  });
  ```

### 5. **Map Method**
- **Transform each element in an array.**
  ```javascript
  var numbers = [1, 2, 3, 4, 5];
  var squares = $.map(numbers, function(element) {
    return element * element;
  });
  ```

### 6. **Trim Method**
- **Remove whitespace from the beginning and end of a string.**
  ```javascript
  var str = "   Hello, World!   ";
  var trimmedStr = $.trim(str);
  ```

### 7. **Now Method**
- **Get the current timestamp.**
  ```javascript
  var timestamp = $.now();
  ```

### 8. **Unique Method**
- **Remove duplicates from an array.**
  ```javascript
  var numbers = [1, 2, 2, 3, 4, 4, 5];
  var uniqueNumbers = $.unique(numbers);
  ```

### 9. **ParseJSON Method**
- **Parse a well-formed JSON string.**
  ```javascript
  var jsonString = '{"name": "John", "age": 30}';
  var parsedData = $.parseJSON(jsonString);
  ```

### 10. **Iterating Over Elements:**

- **Using `each`:**
  ```javascript
  // Iterate over all paragraphs
  $('p').each(function(index, element) {
    console.log(index, $(element).text());
  });
  ```

### 11. **Extend Objects**
- **Merge the contents of two objects.**
  ```javascript
  var obj1 = { foo: "hello" };
  var obj2 = { bar: "world" };
  $.extend(obj1, obj2);
  ```



## Utilities
  
### 1. **Event Handling:**

- **Click Event:**
  ```javascript
  // Click event
  $('#myButton').click(function() {
    alert('Button clicked!');
  });

  // Show a hidden element on button click.
  var hiddenBox = $("#banner-message");
  $("#button-container button").on("click", function(event) {
    hiddenBox.show();
  });
  ```

### 2. **Ajax Requests:**

- **Basic AJAX:**
  ```javascript
  $.ajax({
    url: 'https://api.example.com/data',
    method: 'GET',
    success: function(data) {
      console.log(data);
    },
    error: function(error) {
      console.error('Error:', error);
    }
  });

  // Make an asynchronous HTTP request and update the page.
  $.ajax({
    url: "/api/getWeather",
    data: { zipcode: 97201 },
    success: function(result) {
      $("#weather-temp").html("<strong>" + result + "</strong> degrees");
    }
  });
  ```

### 3. **Animations:**

- **Show/Hide Elements:**
  ```javascript
  // Hide element
  $('#myElement').hide();

  // Show element with animation
  $('#myElement').show(1000); // 1000 milliseconds (1 second)
  ```

---

This guide covers some of the fundamental features and utilities of jQuery 3.7.1. Refer to the [official documentation](https://api.jquery.com/) for a more detailed exploration.

This is just a starting point. jQuery provides a vast array of functions and features. If you have specific questions or if you want examples for a particular feature, feel free to ask!
