# mid

var chime;

var sounds = [];

function preload() {
  soundFormats('m4a');
  for (var i = 0; i < 15; i++) {
    let sound = loadSound('glockenspiel.m4a');
    sound.rate(0.5 * pow(2, i / 12)); // 12-semitone exponential scale

    sounds.push(sound);
  }
}

function setup() {
  createCanvas(400, 400);
  rectMode(CENTER);
}

function draw() {
  background(220);
  noFill();

  for (var i = 0; i < sounds.length; i++) {
    let sound = sounds[i];
    if (sound.isPlaying()) {
      map(sound.currentTime(), 0, sound.duration(), 255, 220);
      for (var x = 10; x < 390; x = x + 70) {
      ellipse(width / sounds. length * (i + 1), 200, x + 20);
      }
    }
  }
}

function mouseMoved() {
  if (mouseY <= 30) {
    sounds[0].play();
  }
  if (mouseY <= 60) {
    sounds[1].play();
  }
  if (mouseY <= 90) {
    sounds[2].play();
  }
  if (mouseY <= 120) {
    sounds[3].play();
  }
  if (mouseY <= 150) {
    sounds[4].play();
  }
  if (mouseY <= 180) {
    sounds[5].play();
  }
  if (mouseY <= 210) {
    sounds[6].play();
  }
  if (mouseY <= 240) {
    sounds[7].play();
  }
  if (key == 'y') {
    sounds[8].play();
  }
  if (key == 'h') {
    sounds[9].play();
  }
  if (key == 'u') {
    sounds[10].play();
  }
  if (key == 'j') {
    sounds[11].play();
  }
  if (key == 'k') {
    sounds[12].play();
  }
  if (key == 'o') {
    sounds[13].play();
  }
  if (key == 'l') {
    sounds[14].play();
  }
}
