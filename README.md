# Historical Tennis Match Outcome Prediction Project

<p align="center">
  <img src="Figures/Robot_Playing_Tennis.png" width="100">
</p>

## Project Overview

This project explores historical ATP tennis match data to identify the key factors that influence match outcomes and to build a machine learning model capable of predicting the winner of future matches.

## Data

The data is sourced from the publically available Jeff Sackmann ATP database (https://github.com/JeffSackmann), which contains detailed match-level data for professional tennis matches.

## Feature Engineering

The data was first cleaned by removing or updating anomolous entries found in the dataset. Most of this anomolous data was missing and could not be sourced using Wikipedia or the official ATP website. Other entries were found like the player Jorge Brian Panta Herreros who's height was found to be 3 cm.

After the completion of the data cleaning the match entries were ordered heirarchically using the start date of the tournament and followed by the round of the tournament ("Q1", "Q2", "Q3", "R128", "R64", "R32", "R16", "QF", "SF", "F"). 

The first objective was to engineer features which could be utilised by the model. The first feature to be engineer was ELO. This tool is most classically used in chess as a way to rank players by their ability. The equation for calculating the ELO was XX. 

$P(A) = \frac{1}{1 + 10^{-(E_A - E_B)/400}}$

Secondly, a surface ELO was calculated in the same way as the ELO but only calculating this metric for each player on a specific surface. 
