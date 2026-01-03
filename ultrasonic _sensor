#define TRIG_PIN 9
#define ECHO_PIN 10

long duration;
float distance_cm;

void setup() {
  Serial.begin(9600);   // Baud rate
  pinMode(TRIG_PIN, OUTPUT);
  pinMode(ECHO_PIN, INPUT);
}

void loop() {
  // Clear trigger pin
  digitalWrite(TRIG_PIN, LOW);
  delayMicroseconds(2);

  // Send trigger pulse
  digitalWrite(TRIG_PIN, HIGH);
  delayMicroseconds(10);
  digitalWrite(TRIG_PIN, LOW);

  // Read echo
  duration = pulseIn(ECHO_PIN, HIGH);

  // Calculate distance
  distance_cm = (duration * 0.0343) / 2;

  // IMPORTANT: Print ONLY NUMBER
  Serial.println(distance_cm);

  delay(1000); // small delay for smooth graph
}
