
# Forecasting Algorithm Selection

## 1. Introduction

This project uses a forecasting algorithm to predict future temperature and humidity readings collected by the DHT11 sensor.

Two forecasting techniques were considered: Simple Moving Average (SMA) and Exponential Moving Average (EMA).

## 2. Simple Moving Average (SMA)

SMA calculates the average of a selected number of previous sensor readings.

Formula:

SMA = Sum of selected readings / Number of readings

Advantages:
- Easy to understand and implement.
- Reduces small fluctuations in sensor readings.
- Suitable for basic time-series forecasting.

Limitations:
- All selected readings have equal importance.
- It may respond slowly to sudden changes in sensor readings.

## 3. Exponential Moving Average (EMA)

EMA is a forecasting technique that gives more importance to recent sensor readings.

Advantages:
- Responds faster to recent changes.
- Gives more weight to newer readings.

Limitations:
- Requires a smoothing factor (alpha).
- Slightly more complicated to implement than SMA.

## 4. Reason for Selecting SMA

SMA was selected for this project because it is simple to understand and suitable for processing temperature and humidity data.

The system uses the latest 36 sensor readings, which represent approximately 6 hours of historical data because the ESP32 sends readings every 10 minutes.

The algorithm uses recursive SMA to generate 24 hourly forecast values for both temperature and humidity.

## 5. Conclusion

In conclusion, SMA was selected because it is straightforward to implement and suitable for demonstrating sensor data forecasting in this IoT project. EMA can be considered in future improvements to compare forecasting performance.
