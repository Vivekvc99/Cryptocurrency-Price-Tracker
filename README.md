
# Current Bitcoin Value Webpage README

## Introduction

This simple webpage displays the current value of Bitcoin in USD. It fetches the value from the Blockchain API and updates it periodically every minute.

## Features

- Lightweight and purely built using HTML and vanilla JavaScript.
- Fetches the current Bitcoin value in USD from Blockchain's public API.
- Automatically updates the displayed Bitcoin value every minute.
- In case of any error or issue with fetching the value, it displays a user-friendly message.

## Implementation Details

### HTML Structure

- The webpage contains a single paragraph `<p>` element that displays the text "Current Bitcoin Value:" followed by a `<span>` element with an `id` of "bitcoin-value". This span will be dynamically updated with the Bitcoin value.

### JavaScript

There are three primary functions:

1. `updateCurrentValue(newValue)`: This function updates the content of the `<span>` with the provided `newValue` and sets a timeout to fetch the new value after one minute.

2. `getCurrentValue()`: This function sends a GET request to the Blockchain API to fetch the current Bitcoin value in USD. Upon successful retrieval, it updates the displayed value using the `updateCurrentValue` function. In case of an error, it updates the displayed value with an error message.

3. `window.onload`: An event listener that calls the `getCurrentValue()` function as soon as the webpage is loaded. This ensures that the Bitcoin value is displayed immediately upon loading the page.

## Usage

To use the webpage:

1. Simply open the HTML file in a web browser.
2. The current Bitcoin value will be displayed and will be updated every minute.

## Dependencies

- This webpage relies on the public API from Blockchain (`https://blockchain.info/q/24hrprice?cors=true`) to fetch the Bitcoin value in USD.
- The webpage uses vanilla JavaScript and doesn't rely on any external libraries or frameworks.

## Considerations

1. Since the webpage queries the API every minute, make sure not to violate any rate limits set by the Blockchain API.
2. Always ensure CORS is enabled when querying external APIs from client-side scripts.

## Future Improvements

- Implement error handling for different types of errors (e.g., network issues, API rate limits, etc.).
- Add visuals or graphs to display historical Bitcoin values.
- Optimize for mobile and other device displays for a more responsive design.

---

Feel free to contribute or raise any issues if you find any bugs or improvements.
