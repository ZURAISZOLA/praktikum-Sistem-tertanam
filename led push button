// C++ code
//
// Deklarasi pin LED
const int ledPins[] = {1, 2, 3, 4, 5}; // LED 1, LED 2, LED 3, LED 4, LED 5
const int buttonPin = 8;               // Pin untuk push button
int buttonState = LOW;                // Variabel untuk membaca status button
int sequence[] = {4, 2, 2, 4, 5, 3, 1, 3, 5, 4, 2}; // Urutan nyala LED

void setup() {
  // Inisialisasi pin LED sebagai output
  for (int i = 0; i < 5; i++) {
    pinMode(ledPins[i], OUTPUT);
    digitalWrite(ledPins[i], HIGH); // LED mati (karena LOW menyalakan)
  }

  // Inisialisasi pin button sebagai input
  pinMode(buttonPin, INPUT_PULLUP);
}

void loop() {
  buttonState = digitalRead(buttonPin);

  if (buttonState == LOW) { // Button ditekan
    for (int i = 0; i < 11; i++) { // 11 urutan running LED
      // Matikan semua LED terlebih dahulu
      for (int j = 0; j < 5; j++) {
        digitalWrite(ledPins[j], LOW);
      }
      
      // Nyalakan LED sesuai urutan
      int ledIndex = sequence[i] - 1; // Karena array LED dimulai dari 0
      digitalWrite(ledPins[ledIndex], HIGH);
      delay(1500); // milisecond
    }
  } else { // Button tidak ditekan
    // Matikan semua LED
    for (int i = 0; i < 5; i++) {
      digitalWrite(ledPins[i], LOW);
    }
  }
}
