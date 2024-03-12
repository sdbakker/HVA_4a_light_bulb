console.log("Pagina geladen");

let getal = 0;
let mysteryNumber = Math.random() * 6;
mysteryNumber = Math.round(mysteryNumber);

const plusKnop = document.querySelector("#plus");
const minKnop = document.querySelector("#min");
const getalVeld = document.querySelector("h1");
const controleerKnop = document.querySelector("#controleer");
const pElement = document.querySelector("#resultaat");

function updateGetalVeld(nieuw)
{
    console.log("nieuw getal: " + nieuw);
    getalVeld.textContent = nieuw;
}

function clearText()
{
    pElement.textContent = "";
}

function controleerGetal() {
    if (getal === mysteryNumber) { 
        console.log("Goed geraden!");
        pElement.textContent = "Goed geraden!";
        clearInterval(timer);
    } else if (getal > mysteryNumber) {
        console.log("helaas, te hoog");
        pElement.textContent = "helaas, te hoog";
    } else {
        console.log("helaas, te laag");
        pElement.textContent = "helaas, te laag";
    }
    setTimeout(clearText, 3000);
}

function pasGetalAan(x)
{
    getal = getal + x;
    updateGetalVeld(getal);
    controleerGetal();
}

function verhoogGetal() {
    getal = getal + 1;
    updateGetalVeld(getal);
    controleerGetal();
}

function verlaagGetal() {
    getal = getal - 1;
    updateGetalVeld(getal);
}

function playAudio(url) {
    console.log("audio speelt: " + url);
}

console.log(mysteryNumber);
const plusAudio = "plus.mp3"
const minAudio = "min.mp3"

plusKnop.addEventListener("click", function() {playAudio(plusAudio)});
minKnop.addEventListener("click", function() { playAudio(minAudio)});
controleerKnop.addEventListener("click", controleerGetal);

//let timer = setInterval(verhoogGetal, 1000);