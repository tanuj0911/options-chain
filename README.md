# Options Chain Tool

This project aims to build an Options Chain Tool that processes real-time market data and calculates various metrics, such as Implied Volatility (IV), to display an options chain screen. The tool will provide a user-friendly web interface where users can select underlying assets, different expiry dates, and filter options based on specific criteria.

## Link to Video and Ppt
https://drive.google.com/drive/folders/1JwjvFekA08XZ4C2eI406XMs2P8lshMa2?usp=sharing

## Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Features](#features)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Installation](#installation)


## Introduction

An option is a derivative product commonly used in trading. It has associated Greeks and can be either a call option or a put option. This project aims to provide a comprehensive options chain tool that allows users to analyze options data in real-time.

## :dart: Problem Statement

The goal of this project is to process market data received over a TCP/IP connection and calculate Implied Volatility (IV) and other relevant metrics. The options chain screen should be displayed as a webpage, similar to platforms like [NSE India Option Chain](https://www.nseindia.com/option-chain). The following requirements should be fulfilled:

- Highlight "in the money" and "out of the money" options differently.
- Provide the ability to select different underlying assets and expiry dates.
- Ensure real-time functionality, where the options chain is updated dynamically as the market data changes, without requiring page reloads.

For Implied Volatility (IV) calculation, the Black Scholes Formula can be used. The following assumptions can be made:

1. Use the Black Scholes Formula for calculating IV from options price.
2. Assume a risk-free interest rate of 5%.
3. To calculate Time To Maturity (TTM) accurately, assume the expiry time to be at 15:30 IST on the expiry day. After the contract expires, TTM will be negative, implying IV as 0.
4. Since options are derivatives of underlying assets, an underlying price will also be published in the same market data stream.

## Features 💡

- Real-time options chain display.
- Selection of underlying assets and different expiry dates.
- Automatic table refresh without page reloads.
- Option to download options chain data as a CSV file.

## :checkered_flag: Usage

To use the Options Chain Tool, follow these steps:

1. Install the necessary dependencies (see [Dependencies](#dependencies)).
2. Run the following command on your CMD - 'java -Ddebug=true -Dspeed="2.0" -classpath ./feed-play-1.0.jar hackathon.player.Main dataset.csv 9011'
3. Run the socket client Python file
4. Start the Python Flask server.
5. The Webpage will be automatically displayed on localhost/3000
6. Access the options chain tool via the provided web interface.
7. Select underlying assets, choose expiry dates, and apply filters as desired.
8. Observe the real-time options chain display and make use of the available features.

## Dependencies

The following dependencies are required to run this project:

- Python (3.6+)
- Flask
- Pandas

## Installation 🖥

To install and set up the Options Chain Tool, follow these steps:

1. Clone the project repository.
2. Install Python (3.6+) and set up a virtual environment (optional but recommended).
3. Install the necessary Python packages using pip or conda (e.g., `pip install flask`).
4. Navigate to the Flask server directory and start the server.
5. Access the options chain tool via the provided web interface.

## Technologies Used

📦 TCP/IP
📦 WebSocket
📦 JavaScript
📦 HTML5
📦 CSS3
📦 Python
📦 Flask


