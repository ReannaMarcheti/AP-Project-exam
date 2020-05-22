# AP-Project-exam
An App I created made up of minigames

onEvent("StartButton", "click", function( ) {
  setScreen("GuessingGame");
  playSound("sound://category_background/fantasy.mp3", true);
  playSound("sound://category_achievements/lighthearted_bonus_objective_3.mp3", false);
});
var number = 4;
hideElement("Click");
onEvent("numberguess", "change", function( ) {
  var userGuess = getText("numberguess");
  if (userGuess == number) {
    setText("userGuess", "Woohoo You Guessed Right!");
    playSound("sound://category_achievements/lighthearted_bonus_objective_2.mp3", false);
    showElement("Click");
    
  } else if ((userGuess > number)) {
    setText("userGuess", "You Need To Guess Lower To Get The Right Number!");
  } else if ((userGuess < number)) {
    setText("userGuess", "You Need To Guess Higher To Get The Right Number!");
  } else {
    setText("userGuess", "Sorry Thats Not It! Please Guess Again!");
  }
});
onEvent("Click", "click", function( ) {
  setScreen("ClickIt");
  playSound("sound://category_achievements/peaceful_win_2.mp3", false);
});
//the kiwi image is not mine//
hideElement("kiwibutton");
onEvent("kiwi", "click", function( ) {
  showElement("kiwibutton");
});
//the player image is not mine//
onEvent("kiwibutton", "click", function( ) {
  setScreen("FindTheWay");
createMaze();
onEvent("move1", "click", function( ) {
  setPosition("player", 214, 414);
  hideElement("move1");
  showElement("move2");
 playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
 showElement("move3");
});
onEvent("move2", "click", function( ) {
  setPosition("player", 200, 310);
  showElement("move4");
  showElement("move5");
  hideElement("move3");
  hideElement("move2");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move4", "click", function( ) {
  setPosition("player", 50, 350);
  hideElement("move5");
  hideElement("move4");
  showElement("move6");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move6", "click", function( ) {
  setPosition("player", 30, 240);
  hideElement("move6");
  showElement("move7");
  showElement("move8");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move7", "click", function( ) {
  setPosition("player", 170, 150);
  hideElement("move7");
  hideElement("move8");
  showElement("move9");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move9", "click", function( ) {
  setPosition("player", 100, 85);
  hideElement("move9");
  showElement("Win");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move3", "click", function( ) {
  setPosition("player", 230, 240);
  hideElement("move2");
  hideElement("move3");
  showElement("move10");
  showElement("move11");
  showElement("move12");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move10", "click", function( ) {
  setPosition("player", 220, 120);
  hideElement("move10");
  hideElement("move11");
  hideElement("move12");
  showElement("move13");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move5", "click", function( ) {
  setPosition("player", 150, 270);
  hideElement("move5");
  hideElement("move4");
  showElement("Restart");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move11", "click", function( ) {
  setPosition("player", 270, 130);
  hideElement("move10");
  hideElement("move11");
  hideElement("move12");
  showElement("move13");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move12", "click", function( ) {
  setPosition("player", 300, 20);
  hideElement("move10");
  hideElement("move11");
  hideElement("move12");
  showElement("move13");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move13", "click", function( ) {
  setPosition("player", 150, 20);
  hideElement("move13");
  showElement("Restart");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("move8", "click", function( ) {
  setPosition("player", 20, 100);
  hideElement("move8");
  showElement("Restart");
   playSound("sound://category_achievements/vibrant_game_achievement_4.mp3", false); 
});
onEvent("Restart", "click", function( ) {
  setPosition("player", 20, 400);
  showElement("move1");

});
onEvent("Win", "click", function( ) {
  setPosition("player", 0, 14);
  hideElement("win");

  showElement("finish");
  showElement("finished");
  playSound("sound://category_alerts/vibrant_game_shutter_alert_2_long_up_down.mp3", false);
});
onEvent("finish", "click", function( ) {
  setScreen("Final");
});
  
});
onEvent("return", "click", function( ) {
  setScreen("MainScreen");
});
function createMaze() {
    penUp();
moveTo(0, 384);
penColor("#FF0000");
penDown();
moveTo(200, 384);
penUp();
moveTo(270, 385);
penDown();
moveTo(400, 385);
penUp();
moveTo(270, 385);
penDown();
moveTo(270, 224);
penUp();
moveTo(200, 224);
moveTo(0, 224);
penDown();
moveTo(100,224);
penUp();
moveTo(150, 224);
penDown()
moveTo(200,224)
moveTo(200,180);
penUp();
moveTo(200, 140);
penDown();
moveTo(200, 80);
moveTo(100, 80);
moveTo(100, 40);
penUp();
moveTo(200, 180);
penDown();
moveTo(100, 180);
penUp();
moveTo(200, 140);
moveTo(150, 140);
penDown();
moveTo(100, 140);
moveTo(100, 120);
penUp();
moveTo(100, 180);
moveTo(50, 180);
penDown();
moveTo(50, 120);
penDown();
moveTo(100, 120);
penUp();
moveTo(100, 40);
penDown();
moveTo(50, 40);
penUp();
moveTo(202, 300);
penDown();
moveTo(80, 300);
penUp();
moveTo(40, 300);
penDown();
moveTo(40, 270);
penUp();
moveTo(40, 300);
penDown();
moveTo(40, 350);
penUp();
moveTo(82, 340);
penDown();
moveTo(220, 340);
moveTo(220, 384);
moveTo(200, 384);
penUp();
moveTo(150, 224);
penDown();
moveTo(150, 270);
moveTo(200, 270);
penUp();
moveTo(220, 280);
penDown();
moveTo(240, 280);
moveTo(240, 320);
penUp();
moveTo(40, 270);
penDown();
moveTo(120, 270);
moveTo(120, 240);
moveTo(150, 240);
penUp();
moveTo(252, 170);
penDown();
moveTo(252, 50);
moveTo(200, 50);
penUp();
moveTo(150, 50);
penDown();
moveTo(130, 50);
moveTo(130, 30);
moveTo(120, 30);
moveTo(120, 20);
moveTo(50, 20);
penUp();
moveTo(180, 30);
penDown();
moveTo(280, 30);
moveTo(280, 100);
moveTo(300, 100);
moveTo(300, 180);
penUp();
moveTo(250, 220);
penDown();
moveTo(250, 200);
moveTo(280, 200);
moveTo(280, 180);
penUp();
moveTo(140, 114);
penDown();
moveTo(170, 114);
moveTo(170, 130);
penUp();
moveTo(140, 114);
penDown();
moveTo(140, 100);
penUp();
moveTo(140, 100);
penUp();
moveTo(80, 100);
penDown();
moveTo(50, 100);
moveTo(50, 80);
moveTo(0, 80);
penUp();
moveTo(20, 50);
penDown();
moveTo(50, 50);
moveTo(50, 0);
penUp();
moveTo(200, 140);
penDown();
moveTo(200, 180);
penUp();
moveTo(50, 124);
penDown();
moveTo(50, 100);
penUp();
moveTo(270, 385);
penDown();
moveTo(220, 480);
penUp();
moveTo(80, 300);
penDown();
moveTo(40,270);
penUp();
hideElement("move2");
hideElement("move3");
hideElement("move4");
hideElement("move5");
hideElement("move6");
hideElement("move7");
hideElement("move8");
hideElement("move9");
hideElement("Win");
hideElement("Restart");
hideElement("move11");
hideElement("move10");
hideElement("move12");
hideElement("move13");
  hideElement("finish");
  hideElement("finished");
  
}


