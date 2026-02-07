# Valentine-for--hirva-27
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <img src="https://gifdb.com/images/high/cute-love-bear-roses-ou7zho5oosxnpo6k.gif" alt="Valentine Gif">
        <h1>Will You Be My Valentine?</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="handleYes()">Yes ❤️</button>
            <button id="noBtn" onclick="handleNo()">No 💔</button>
        </div>
    </div>
let noCount = 0;

let noTexts = [
    "No 💔",
    "Are you sure?",
    "Really sure?",
    "Think again!",
    "Last chance...",
    "Please 😢",
    "Don’t break my heart 💔",
    "Say yes 😭",
    "Pretty please ❤️",
    "Just say yes 😍"
];

function noFunction() {
    let yesBtn = document.getElementById("yesBtn");
    let noBtn = document.getElementById("noBtn");

    // Increase size of YES button
    yesBtn.style.transform = `scale(${1 + noCount * 0.15})`;

    // Change NO button text
    noBtn.innerText = noTexts[noCount] || "Please say YES ❤️";

    noCount++;

    // Optional: move NO button randomly
    // let randomX = Math.random() * 200 - 100;
    // let randomY = Math.random() * 200 - 100;
    // noBtn.style.transform = `translate(${randomX}px, ${randomY}px)`;
}

function yesFunction() {
    window.location.href = "yes.html";
}
