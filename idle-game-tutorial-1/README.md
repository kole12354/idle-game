<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Gold Miner</title>
  </head>
  <body>
    <p>0 Gold Mined</p>
    <button>Mine Gold</button>
  </body>
</html>

var gameData = {
  gold: 0,
  goldPerClick: 1
}

var gameData = {
  gold: 0,
  goldPerClick: 1
}

function mineGold() {
  gameData.gold += gameData.goldPerClick
}
document.getElementById("goldMined").innerHTML = gameData.gold + " Gold Mined"
<button onclick="buyGoldPerClick()" id="perClickUpgrade">Upgrade Pickaxe (Currently Level 1) Cost: 10 Gold</button>
function buyGoldPerClick() {
  if (gameData.gold >= gameData.goldPerClickCost) {
    gameData.gold -= gameData.goldPerClickCost
    gameData.goldPerClick += 1
    gameData.goldPerClickCost *= 2
    document.getElementById("goldMined").innerHTML = gameData.gold + " Gold Mined"
    document.getElementById("perClickUpgrade").innerHTML = "Upgrade Pickaxe (Currently Level " + gameData.goldPerClick + ") Cost: " + gameData.goldPerClickCost + " Gold"
  }
}

var gameData = {
  gold: 0,
  goldPerClick: 1,
  goldPerClickCost: 10
  
  var mainGameLoop = window.setInterval(function() {
  mineGold()
}, 1000)
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Gold Miner</title>
  </head>
  <body>
    <p id="goldMined">0 Gold Mined</p>
    <button onclick="mineGold()">Mine Gold</button>
    <button onclick="buyGoldPerClick()" id="perClickUpgrade">Upgrade Pickaxe (Currently Level 1) Cost: 10 Gold</button>
    <script src="main.js" charset="utf-8" type="text/javascript"></script>
  </body>
  var gameData = {
  gold: 0,
  goldPerClick: 1,
  goldPerClickCost: 10
}

function mineGold() {
  gameData.gold += gameData.goldPerClick
  document.getElementById("goldMined").innerHTML = gameData.gold + " Gold Mined"
}

function buyGoldPerClick() {
  if (gameData.gold >= gameData.goldPerClickCost) {
    gameData.gold -= gameData.goldPerClickCost
    gameData.goldPerClick += 1
    gameData.goldPerClickCost *= 2
    document.getElementById("goldMined").innerHTML = gameData.gold + " Gold Mined"
    document.getElementById("perClickUpgrade").innerHTML = "Upgrade Pickaxe (Currently Level " + gameData.goldPerClick + ") Cost: " + gameData.goldPerClickCost + " Gold"
  }
}

var mainGameLoop = window.setInterval(function() {
  mineGold()
}, 1000)
  var saveGameLoop = window.setInterval(function() {
  localStorage.setItem("goldMinerSave", JSON.stringify(gameData))
}, 15000)
  var savegame = JSON.parse(localStorage.getItem("goldMinerSave"))
if (savegame !== null) {
  gameData = savegame
}
  if (typeof savegame.dwarves !== "undefined") gameData.dwarves = savegame.dwarves;

}

function buyGoldPerClick() {
  if (gameData.gold >= gameData.goldPerClickCost) {
    gameData.gold -= gameData.goldPerClickCost
    gameData.goldPerClick += 1
    gameData.goldPerClickCost *= 2
  }
}

