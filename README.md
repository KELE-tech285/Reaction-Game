# Reaction-Game
This project is a competitive reaction game built using an Arduino, two buttons, three LEDs, and a 16x2 I2C LCD. Two players face off to test their reflexes across multiple rounds — but press too early and you'll hand the round to your opponent!

🕹️ Features
2-player reaction challenge with scoring

Randomized LED countdown to prevent timing prediction

Early press penalty system

LCD displays round info, scores, and winner

Game ends after 5 rounds

🧰 Hardware Required
|Component	     | Quantity                        |
|----------------|---------------------------------|
|Arduino Uno	   |1                                |
|16x2 I2C LCD	   |1                                |
|Push Buttons    |2                                |
|10kΩ Resistors	 |2 (optional, if not using INPUT) |
|LEDs	           |3                                |
|Resistors (220Ω)|3 (for LEDs)                     |
|Jumper Wires	   |Several                          |
|Breadboard	     |1                                |

⚡ Wiring
Buttons
|Pin	    |    Arduino |
|---------|------------|
|Button 1 |D2          |
|Button 2 |D4          |

LEDs
|LED   | 	Arduino |
|------|----------|
|LED 1 |D7        |
|LED 2 |D8        |
|LED 3 |D9        |

LCD (I2C)
|LCD Pin  |	Arduino |
|---------|---------|
|SDA      |A4       |
|SCL      |A5       |

Ensure your I2C LCD address is 0x27. Use an I2C scanner sketch if unsure.

🧠 How It Works
Start Game: Both players press their buttons simultaneously to begin.

LED Countdown: LEDs turn off one by one with a random delay (0.5–2 seconds).

Reaction Phase: After all LEDs turn off, first to press wins the round.

Early Press: If a player presses too soon, they lose the round.

Scoring: Game runs for 5 rounds. LCD shows scores and declares a winner.

📜 How to Play
Upload the code to your Arduino.

Press both buttons to start the game.

Watch the LED countdown.

As soon as all LEDs are off, press your button.

First to react scores a point. If you press early, your opponent scores.

Game ends after 5 rounds — press both buttons again to restart.

🧾 Key Code Behavior
Debouncing: Prevents false readings from noisy button signals.

Random Delay: Each LED has a randomized delay to prevent button mashing.

LCD Feedback: Displays current round, scores, and outcome of each round.

Serial Output: For debugging via Serial Monitor at 9600 baud.

🧪 Customization Ideas
Add a buzzer for sound feedback.

Increase maxRounds for a longer game.

Adjust LED delays for difficulty.

📷 Preview (Optional)
Add a photo of your hardware setup and LCD display here!

🧰 Libraries Used
LiquidCrystal_I2C

Install via Library Manager in the Arduino IDE:

Sketch > Include Library > Manage Libraries > Search for "LiquidCrystal_I2C" 


![IMG_20250605_190236](https://github.com/user-attachments/assets/1dade741-9081-4dea-9fe0-2ce73b3bf9c3)
![IMG_20250605_190243](https://github.com/user-attachments/assets/9dede18c-ca95-49e9-9c0d-50a0bcf292af)
![IMG_20250605_190253](https://github.com/user-attachments/assets/f95dc1fd-22a1-4923-9175-6dd5529b60e3)
![IMG_20250605_190304](https://github.com/user-attachments/assets/35c98a30-b914-42eb-9bfa-eb5f180aff67)
![IMG_20250303_182646](https://github.com/user-attachments/assets/f5ee3deb-7606-4774-9333-5a3eb4b14746)
![IMG_20250605_190233](https://github.com/user-attachments/assets/8544c0d6-1a03-4b83-be9e-b56efb7e3659)
