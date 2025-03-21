# Live Black-Scholes Implementation

---

## Overview

This project implements a live Black-Scholes pricing model using python, designed to price European-style call options in real-time using market data from Yahoo Finance. The model's performance is compared to an existing Black-Scholes implementation to evaluate its accuracy.

---

## Motivation and Background

The motivation behind creating this Black-Scholes pricing model stems from my deep interest in the intersection of finance and technology. I’ve always been fascinated by how mathematical models can be applied to real-world financial markets to manage risk and make informed investment decisions. As a student eager to explore quantitative finance, I wanted to gain hands-on experience by implementing one of the most fundamental models in options pricing. 

Working with live market data and applying advanced computational tools like **JAX** made this project especially appealing. By building this model, I aimed to enhance my understanding of option pricing theory, improve my programming skills, and explore how modern computing techniques can optimize financial calculations. 

This project prepares me for a future career in quantitative finance, where I hope to contribute to the evolution of financial modeling and risk management strategies.

---

## Table of Contents

1. [Introduction](#1-introduction)  
2. [Data Collection](#2-data-collection)  
3. [Black-Scholes Model](#3-black-scholes-model)
4. [Implied Volatility Calculation Using Newton Method](#4-Implied-Volatility-Calculation-Using-Newton-Method)  

---

## 1. Introduction

Accurately pricing options is a critical component of modern financial markets, enabling traders and investors to manage risk and make informed decisions. The **Black-Scholes model**, introduced in 1973 by Fischer Black, Myron Scholes, and Robert Merton, is one of the most widely used mathematical models for option pricing. It calculates the theoretical price of European-style options by considering factors such as the underlying asset price, strike price, time to expiration, volatility, risk-free interest rate, and dividends.

This project implements a live Black-Scholes pricing model using **JAX**, a high-performance library for automatic differentiation and numerical computing. The model is designed to price call options in real-time using market data from Yahoo Finance, and its performance is compared to an existing Black-Scholes implementation.

---

## 2. Data Collection

Data collection is crucial for ensuring the model operates with accurate and up-to-date market information. This section focuses on gathering all the necessary data from Yahoo Finance. The Yahoo Finance library within python was used to gather the latest market data each time this file is run, no need to manually download any data since it automatically is imported into the python script. All that is required is to input the ticker for a particular stock then run the script where data for all availible options on yahoo finance will be collected along with the underlying stock's data as well as current treasury data for the risk free rate. 

---

## 3. Black-Scholes Model

This section describes the mathematical formulas behind the Black-Scholes model and details its implementation in Python using JAX. The Black-Scholes model formulas for call and put options are presented here. The formulas calculate the option price using factors like stock price, strike price, volatility, time to expiration, risk-free rate, and dividend yield. This section serves as a theoretical foundation, explaining the core equations driving the pricing model. After implementing this model in python, it was compared to existing code from the BlackScholes library already existing in python. Performance was very similar, as it should since it is effectivly the same model. NOTE: Although the Black-Scholes model was created to price European style options, in this case we are using it with data from American style options. This is only because of data aquisition, I found the code pulling stock data from yahoo finance much more useful to build off of for future project so I decided to use this American option data but assume that it is a European style option. Since the goal of this project was to create my own Black-Scholes model and just compare it to an existing model, this note does not affect the model since both models used the same input. Therefore, this model does not intend to be (and would perform poorly) as any kind of trading tool, it was only made so I could develop my skills and familiarise myself more with the Black-Scholes model.

---

## 4. Implied Volatility Calculation Using Newton Method
In the Implied Volatility (IV) calculation section, we use the Newton-Raphson method to estimate the implied volatility for each option based on its market price. The method iteratively refines an initial guess for volatility by minimizing the difference between the theoretical price (calculated using the Black-Scholes model) and the actual market price of the option. The process continues until the difference between the theoretical and market prices is sufficiently small, indicating convergence. This section demonstrates how to compute IV for individual options and compare the calculated values with the market's implied volatility.

---

## 4. Conclusion

The overall goal of this project was to create a robust, real-time Black-Scholes pricing model that uses live market data and modern computational techniques. The data collection ensures that the model works with accurate, up-to-date information, while the implementation and comparison sections focus on validating the model's effectiveness. The project not only enhanced my understanding of options pricing but also showcases how computational tools like JAX can optimize financial calculations.








