# Volatility Modelling in Continuous Time (Heston & Dupire Models)

## Overview
This project explores **stochastic volatility modelling** using the **Heston model** and its calibration to the **Dupire local volatility model**.  
The work involves building option price and implied volatility surfaces, extracting market features such as skew and term structure, and comparing dynamic pricing behaviour across models.  

The project is structured into five main questions, each corresponding to a key stage of the modelling workflow.

---

## Project Structure

- **Task 1 – Approach and Model Setup**  
  Introduction to the Heston model, stochastic variance dynamics, and implementation in QuantLib.  

- **Task 2 – Option Price Surface**  
  Construction of a \( 50 \times 50 \) grid of European call option prices across strikes and maturities.  
  Includes discussion of moneyness effects, convexity, and ATM sensitivity.  

- **Task 3 – Implied Volatility Surface**  
  Extraction of implied volatilities from option prices by inverting the Black–Scholes model.  
  Analysis of volatility skew/smile and term structure.  

- **Task 4 – Dupire Local Volatility Pricing**  
  Calibration of a local volatility surface from implied volatilities and pricing of out-of-grid options.  
  Comparison of Dupire and Heston pricing outcomes.  

- **Task 5 – Dynamic Pricing with Evolving Spot Prices**  
  Simulation of asset paths under Heston dynamics and rolling option re-pricing.  
  Comparison of static Dupire calibration vs. dynamic Heston process.  

---

## Key Models

- **Heston Model (Stochastic Volatility)**
  - Captures mean-reverting variance and leverage effect.
  - Produces realistic option smiles and skews.

- **Dupire Local Volatility Model**
  - Perfectly fits the implied volatility surface.
  - Deterministic framework, good for calibration but less adaptive to shocks.

---

## Results & Insights

- **Heston** provides a **dynamic stochastic framework** capturing volatility clustering and reversion.  
- **Dupire** offers **exact calibration to market IVs**, but overestimates prices when variance reverts.  
- The combination highlights trade-offs between **realism** (Heston) and **calibration accuracy** (Dupire).  

---

## Dependencies

- Python 3.x  
- [QuantLib-Python](https://www.quantlib.org/python.shtml)  
- NumPy, Pandas, Matplotlib  

To install QuantLib-Python:

```bash
pip install QuantLib
