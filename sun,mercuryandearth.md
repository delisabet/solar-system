solar-system
===========
float rotangl = 0;
// Angle of rotation 
void setup() {
  size(600, 400);
  smooth();
}

void draw() {
  background(127, 99, 95); 
  noStroke();

  // Sol
  translate(width/2, height/2);
  fill(255, 200, 50);
  ellipse(0, 0, 50, 50);

  // Earth 
  pushMatrix();
  rotate(rotangl);
  translate(160, 0);
  fill(54, 39, 127);
  ellipse(0, 0, 25, 25);

  // Earth Moon 

  pushMatrix(); 
  rotate(-rotangl*4);
  translate(20, 0);
  fill(108, 79, 255);
  ellipse(0, 0, 6, 6);
  popMatrix();
  popMatrix();

  // MARS
  pushMatrix();
  rotate(rotangl*1.5);
  translate(80, 0);
  fill(255, 97, 76);
  ellipse(0, 0, 15, 15);

//Mars moon
  pushMatrix(); 
  rotate(-rotangl*3);
  translate(20, 0);
  fill(127, 15, 0);
  ellipse(0, 0, 6, 6);
  popMatrix();
  popMatrix();

  rotangl += 0.01;
}

