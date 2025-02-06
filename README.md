# Quote Generator

## Description
A simple Quote Generator application built using HTML, CSS, and JavaScript. This project fetches a random quote from an external API and allows users to share the quote on Twitter.

## Features
- 🎉 Fetches a new random quote at the click of a button.
- 📝 Displays both the quote and its author.
- 🐦 Tweet the displayed quote directly from the app.

## Demo
![📸 Quote Generator Screenshot](#)

## Technologies Used
- **📝 HTML**: Structure of the application.
- **🎨 CSS**: Styling and layout.
- **🤖 JavaScript**: Logic for fetching quotes and sharing on Twitter.
- **🌐 DummyJSON API**: Provides random quotes.

## How to Use
1. 📂 Clone the repository or download the files.
2. 🗃️ Open `index.html` in a web browser.
3. 🔄 Click the **New Quote** button to get a random quote.
4. 🐦 Click the **Tweet** button to share the quote on Twitter.

## Code Explanation
### 📚 HTML
- Provides the structure for displaying the quote, author, and buttons.

### 🎨 CSS
- Styles the layout of the quote box.

### 💻 JavaScript
```javascript
const quote = document.getElementById("quote")
const author = document.getElementById("author")

const api_url = "https://dummyjson.com/quotes/random";

async function getQuote(url) {
    const response = await fetch(url);
    var data = await response.json();
    console.log(data);
    quote.innerHTML = data.quote;
    author.innerHTML = data.author;
}

getQuote(api_url);

function tweet() {
    window.open("https://twitter.com/intent/tweet?text=" + quote.innerHTML + " --by " + author.innerHTML, "Tweet Window", "width=600, height=300");
}
```


## Improvements
- 🌟 Add better styling for enhanced UX.
- 🌐 Allow users to copy the quote to the clipboard.
- 📚 Use additional APIs to provide more quotes.


