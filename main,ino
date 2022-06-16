int r = 9;
int g = 10;
int b = 11;

int defaultLevel = 5;
int maxAnalogPerDefaultLevel = 255 / defaultLevel;

void setup() {
  Serial.begin(9600);

  pinMode(r, OUTPUT);
  pinMode(g, OUTPUT);
  pinMode(b, OUTPUT);
}

void loop() {
  int illuminance = analogRead(A0);
  int level = illuminance / 10;
  Serial.println(level);
  
  int n = -level + defaultLevel;
  Serial.println(n);
  Serial.println();

  if (n < 0) n = 0;
  int result = maxAnalogPerDefaultLevel * n;
  digitalWrite(r, result);
//  digitalWrite(g, result);
//  digitalWrite(b, result);
}
