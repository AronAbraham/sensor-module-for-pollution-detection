# Raspberry Pi 3 - DHT11 and MQ135 Sensors - Thingspeak Integration

This project demonstrates how to connect a DHT11 temperature and humidity sensor along with an MQ135 gas sensor to a Raspberry Pi 3 board and send the data to a Thingspeak channel.

## Hardware Setup

### DHT11 Sensor
- Connect the DHT11 sensor to the Raspberry Pi 3:
  - DHT11 VCC pin -> Raspberry Pi 3 3.3V pin
  - DHT11 DATA pin -> Raspberry Pi 3 GPIO 23 (pin 16)
  - DHT11 GND pin -> Raspberry Pi 3 GND pin

### MQ135 Sensor
- Connect the MQ135 sensor to the Raspberry Pi 3:
  - MQ135 VCC pin -> Raspberry Pi 3 5V pin
  - MQ135 DATA pin -> Raspberry Pi 3 Analog pin (e.g., GPIO 2, pin 3)
  - MQ135 GND pin -> Raspberry Pi 3 GND pin

## Software Setup

1. Install necessary libraries:
   - adafruit_dht
   - requests

2. Get Thingspeak API key:
   - Sign up on Thingspeak (if you haven't already).
   - Create a new channel.
   - Note down the API key.

## Running the Code

1. Copy the provided Python script (`sense.py`) to your Raspberry Pi 3.
2. Open the script and replace 'API_KEY' with your actual Thingspeak API key.
3. Upload the script to your Raspberry Pi 3.
4. Run the script.

## Thingspeak Channel

To view the data on Thingspeak:

- Go to [Thingspeak website](https://thingspeak.com).
- Sign in to your account.
- Navigate to your channel.

## Thingspeak URL

The Thingspeak URL for updating the channel should be constructed as follows:
 url = f"https://api.thingspeak.com/update?api_key={API_KEY}&field2={temperature}&field3={humidity}&field4={co2}"

