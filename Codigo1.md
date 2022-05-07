int w, w2, h, h2, s, b;
float m1, m2, m3;

void setup() {
  size(1000, 1200);
  noStroke ();

  colorMode (HSB, 360, 100, 100);
  m1 = int(random(360));
  m2 = m1+120;
  m3 = m2+120;
  if (m2 > 360)
    m2= m2-360;
  else if (m3 >360)
    m3= m3-360;
  s = b = 100;
  println (m1, m2, m3);

  w=width;
  w2=width/2;
  h=height;
  h2=height/2;
  if (w==h)
    h=w/2;
  else if (h >w)
    h=h2;
}

void draw() {
  fill (155);
  rect(0, 0, w2, h);
  fill (55);
  ellipse(2*w/8, 2*h/4, w2, h);
  fill (155);
  quad(2*w/8, 0, w/2, h/2, 2*w/8, h, 0, h/2);
  fill (55);
  rect(w/8, h/4, 2*w/8, 2*h/4);
  fill (155);
  rect(4*w/8, 0, w2, h);
  fill (55);
  ellipse(6*w/8, h/2, w2, h);
  fill (155);
  quad(6*w/8, 0, w, h/2, 6*w/8, h, w2, h/2);
  fill (55);
  rect(5*w/8, h/4, 2*w/8, 2*h/4);
  if (mouseX > w/8 && mouseX < 3*w/8 && mouseY > h/4 && mouseY < 3*h/4) {
    fill (m1, s, b);
    rect(0, 0, w2, h);
    fill (m2, s, b);
    ellipse(2*w/8, 2*h/4, w2, h);
    fill (m1, s, b);
    quad(2*w/8, 0, w/2, h/2, 2*w/8, h, 0, h/2);
    fill (m3, s, b);
    rect(w/8, h/4, 2*w/8, 2*h/4);
    fill (0);
    rect(4*w/8, 0, w2, h);
    fill (255);
    ellipse(6*w/8, 2*h/4, w2, h);
    fill (0);
    quad(6*w/8, 0, w, h/2, 6*w/8, h, w2, h/2);
    fill (255);
    rect(5*w/8, h/4, 2*w/8, 2*h/4);
  } else if (mouseX > 5*w/8 && mouseX < 7*w/8 && mouseY> h/4 && mouseY < 3*h/4) {
    fill (0);
    rect(0, 0, w2, h);
    fill (255);
    ellipse(2*w/8, 2*h/4, w2, h);
    fill (0);
    quad(2*w/8, 0, w/2, h/2, 2*w/8, h, 0, h/2);
    fill (255);
    rect(w/8, h/4, 2*w/8, 2*h/4);
    fill (m1, s, b);
    rect(w/2, 0, w2, h);
    fill (m2, s, b);
    ellipse(6*w/8, h/2, w2, h);
    fill (m1, s, b);
    quad(6*w/8, 0, w, h/2, 6*w/8, h, w2, h/2);
    fill (m3, s, b);
    rect(5*w/8, h/4, 2*w/8, 2*h/4);
  }
}
