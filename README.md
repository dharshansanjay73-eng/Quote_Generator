# Quote_Generator
## Date:14/3/2026
## Objective:
To create a simple thirukkural generator using HTML, CSS, and JavaScript that displays a new random thirukkural each time a button is clicked — similar to daily quote sections on blogs or productivity apps.

## Tasks:

### 1. Create the HTML Structure:
<ul>
  <li>Add a heading Thirukkural Generator</li>
  <li>Use a div or p to display the Thirukkural (Tamil couplet).</li>
  <li>Use another p or span to display the meaning or explanation.</li>
  <li>Add a button labeled “Get Thirukkural”.</li>
  <li>Add a label showing the Kural number.</li>
</ul>

### 2. Style the Layout Using CSS:

<ul>
  <li>Center everything on the page using Flexbox.</li>
  <li>Style the quote box with:
  <ul type="square">
    <li>Padding</li>
    <li>Background color</li>
    <li>Rounded borders</li>
    <li>Soft shadow</li>
    <li>Add hover effects for the button.</li>
  </ul>
  </li>
</ul>

### 3. Add JavaScript Functionality:
<ul>
  <li>Store an array of Thirukkural objects containing:
  <ul type="square">
    <li>Kural number</li>
    <li>Kural Meaning</li>
  </ul>
  </li>
  <li>When the button is clicked:
  <ul type="square">
    <li>Generate a random index using Math.random().</li>
    <li>Retrieve the corresponding Thirukkural object.</li>
    <li>Display the Kural number and meaning in the HTML.</li>
    <li>Update content dynamically using innerText.</li>
  </ul>
  </li>
</ul>

## Code:
```
<!DOCTYPE html>
<html lang="ta">
<head>
<meta charset="UTF-8">
<title>Thirukkural Generatorx</title>
<style>
    body {
        margin: 0;
        padding: 0;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background: #f2cccc;
        font-family: Arial, sans-serif;
        color: darkred;
    }

    h1 {
        margin-bottom: 20px;
    }

    .box {
        background: white;
        width: 350px;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 4px 8px rgba(51, 3, 3, 0.2);
        text-align: center;
        background-color: rgb(237, 227, 141);
    }

    #kuralNumber {
        font-weight: bold;
        color: #09d506;
        margin-bottom: 10px;
    }

    #kural {
        font-size: 20px;
        margin-bottom: 15px;
        line-height: 1.5;
        color: rgb(33, 3, 143);
    }

    #meaning {
        color: #e28e8e;
        margin-bottom: 20px;
    }

    button {
        padding: 10px 20px;
        border: none;
        border-radius: 6px;
        background: #66a4e6;
        color: rgb(234, 101, 101);
        font-size: 16px;
        cursor: pointer;
        transition: 0.3s;
    }

    button:hover {
        background: #9ac4f0;
    }
</style>
</head>

<body>

<h1>Thirukkural Generator</h1>

<div class="box">
    <p id="kuralNumber">Kural No. --</p>
    <p id="kural"> Press this to get a Thirukkural</p>
    <p id="meaning"></p>
    <button onclick="generateKural()">Thirukkural Peravum</button>
</div>

<script>
const kurals = [
    {
        number: 1,
        kural: "அகர முதல எழுத்தெல்லாம் ஆதி\nபகவன் முதற்றே உலகு",
        meaning: "All laetters begin with 'A'; likewise, the world begins with the eternal God."
    },
    {
        number: 2,
        kural: "கற்றதனால் ஆய பயனென்கொல் வாலறிவன்\nநற்றாள் தொழாஅர் எனின்",
        meaning: "What use is learning if one does not worship the feet of the One with true wisdom?"
    },
    {
        number: 3,
        kural: "அறத்தொடு நடுவுவகை நீத்தல் மறத்தொடு\nமாநிலம் சூழ்வார்க்கு இல்",
        meaning: "Those who abandon virtue and justice have no real greatness."
    }
];

function generateKural() {
    const randomIndex = Math.floor(Math.random() * kurals.length);
    const k = kurals[randomIndex];

    document.getElementById("kuralNumber").innerText = "Kural Number: " + k.number;
    document.getElementById("kural").innerText = k.kural;
    document.getElementById("meaning").innerText = k.meaning;
}
</script>

</body>
</html>
```
## Output:
![alt text](image-1.png)

## Result:
A simple quote generator using HTML, CSS, and JavaScript that displays a new random motivational quote each time a button is clicked — similar to daily quote sections on blogs or productivity apps is created successfully.
