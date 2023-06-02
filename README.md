# A-C-programming-for-paralysis-patient-using-arduinio-two-wheel-chair-and-IR-sensors
hello everyone here i am make public an arduino programming for paralysis with the help of two wheel chair and IR sensors and it will also work in order to two motor line follower.


// Motor A connections
const int motorAPin1 = 2; // Pin for motor A, input 1
const int motorAPin2 = 3; // Pin for motor A, input 2
const int motorAEnablePin = 9; // Pin for motor A, enable

// Motor B connections
const int motorBPin1 = 4; // Pin for motor B, input 1
const int motorBPin2 = 5; // Pin for motor B, input 2
const int motorBEnablePin = 10; // Pin for motor B, enable

void setup() {
  // Set motor control pins as outputs
  pinMode(motorAPin1, OUTPUT);
  pinMode(motorAPin2, OUTPUT);
  pinMode(motorAEnablePin, OUTPUT);
  pinMode(motorBPin1, OUTPUT);
  pinMode(motorBPin2, OUTPUT);
  pinMode(motorBEnablePin, OUTPUT);
}

void loop() {
  // Move forward
  moveForward();
  delay(2000); // Wait for 2 seconds

  // Stop
  stopMotors();
  delay(1000); // Wait for 1 second

  // Move backward
  moveBackward();
  delay(2000); // Wait for 2 seconds

  // Stop
  stopMotors();
  delay(1000); // Wait for 1 second
}

void moveForward() {
  digitalWrite(motorAPin1, HIGH);
  digitalWrite(motorAPin2, LOW);
  digitalWrite(motorAEnablePin, HIGH);
  digitalWrite(motorBPin1, HIGH);
  digitalWrite(motorBPin2, LOW);
  digitalWrite(motorBEnablePin, HIGH);
}

void moveBackward() {
  digitalWrite(motorAPin1, LOW);
  digitalWrite(motorAPin2, HIGH);
  digitalWrite(motorAEnablePin, HIGH);
  digitalWrite(motorBPin1, LOW);
  digitalWrite(motorBPin2, HIGH);
  digitalWrite(motorBEnablePin, HIGH);
}

void stopMotors() {
  digitalWrite(motorAPin1, LOW);
  digitalWrite(motorAPin2, LOW);
  digitalWrite(motorAEnablePin, LOW);
  digitalWrite(motorBPin1, LOW);
  digitalWrite(motorBPin2, LOW);
  digitalWrite(motorBEnablePin, LOW);
}
