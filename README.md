### Hello World in Flask with HTML, CSS, and JavaScript

```
Created by:
Name: Shreyas B R
```

---

### What is Flask?

- **Flask** is a lightweight Python web framework that allows you to build web applications.
- You can combine Flask with **HTML**, **CSS**, and **JavaScript** to create dynamic, interactive, and styled web pages.

---

### Basic Folder Structure for Flask with HTML, CSS, and JavaScript

Here’s the basic structure of a Flask app that includes HTML, CSS, and JavaScript:

```
/flask_hello_html_css_js
    /static
        /css
            style.css
        /js
            script.js
    /templates
        hello.html
    app.py
```

- **app.py**: The main Python file for the Flask app.
- **templates/**: Folder for HTML files.
- **static/css/**: Folder for CSS files.
- **static/js/**: Folder for JavaScript files.

---

### Steps to Create a "Hello World" App in Flask with HTML, CSS, and JavaScript

1. **Install Flask**:
   - Install Flask using pip:
     ```bash
     pip install flask
     ```

2. **Create the Project Folder**:
   - Create a new folder called `flask_hello_html_css_js`.

3. **Create the `app.py` File**:
   - Inside the project folder, create a file called `app.py` with the following code:

   ```python
   from flask import Flask, render_template

   app = Flask(__name__)

   @app.route('/')
   def hello_world():
       return render_template('hello.html')

   if __name__ == "__main__":
       app.run(debug=True)
   ```

4. **Create the `templates` Folder**:
   - Inside the project folder, create a folder called `templates` and add a file `hello.html`.

5. **Create the `hello.html` File**:
   - Inside the `templates` folder, create the `hello.html` file and add the following code:

   ```html
   <!DOCTYPE html>
   <html>
   <head>
       <title>Hello Flask</title>
       <link rel="stylesheet" type="text/css" href="{{ url_for('static', filename='css/style.css') }}">
       <script type="text/javascript" src="{{ url_for('static', filename='js/script.js') }}"></script>
   </head>
   <body>
       <h1>Hello, World!</h1>
       <p>Welcome to Flask with HTML, CSS, and JavaScript!</p>
       <button onclick="displayMessage()">Click Me</button>
       <p id="message"></p>
   </body>
   </html>
   ```

   - The `link` tag links the **CSS** file, and the `script` tag links the **JavaScript** file from the **static** folder.
   - A button is added that will trigger a JavaScript function when clicked.

6. **Create the `static/css` Folder**:
   - Inside the project folder, create a folder called `static`, and inside it, create a folder called `css`. This is where the CSS file will be stored.

7. **Create the `style.css` File**:
   - Inside the `static/css` folder, create a file called `style.css` and add the following CSS code:

   ```css
   body {
       background-color: #f9f9f9;
       font-family: Arial, sans-serif;
       text-align: center;
   }

   h1 {
       color: blue;
   }

   p {
       color: green;
       font-size: 18px;
   }

   button {
       padding: 10px 20px;
       background-color: orange;
       border: none;
       color: white;
       cursor: pointer;
   }
   ```

8. **Create the `static/js` Folder**:
   - Inside the `static` folder, create a folder called `js`. This is where the JavaScript file will be stored.

9. **Create the `script.js` File**:
   - Inside the `static/js` folder, create a file called `script.js` and add the following JavaScript code:

   ```javascript
   function displayMessage() {
       document.getElementById("message").innerHTML = "Hello from JavaScript!";
   }
   ```

   - This JavaScript function changes the text of the `<p>` element with the ID "message" when the button is clicked.

10. **Run the Flask App**:
    - Open a terminal in your project folder and run:
      ```bash
      python app.py
      ```

11. **View the App in a Browser**:
    - Open your browser and go to `http://127.0.0.1:5000/`. You should see a styled page with a button that, when clicked, displays a message using JavaScript.

---

### Explanation of Folder Structure:

- **app.py**: The main Python file that defines the Flask routes and renders the HTML template.
- **templates/**: The folder where HTML files are stored.
- **static/css/**: The folder where static CSS files are stored.
- **static/js/**: The folder where static JavaScript files are stored.

---

### Key Points:

- Flask allows you to integrate **HTML**, **CSS**, and **JavaScript** to build interactive and styled web applications.
- **CSS** is used to style the content, and **JavaScript** adds interactivity (like responding to button clicks).
- Flask serves these static files from the **static** folder while rendering the HTML from the **templates** folder.

---

**End of Document** ✨
