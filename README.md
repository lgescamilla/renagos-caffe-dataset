# Renago’s Caffe Dataset

This repository contains sample point-of-sale (POS) data used throughout the guidebook *Mac-Ready Power BI: Build Dashboards Without Windows*. The dataset is based on a fictional café in Santa Monica, modeled after real-world reporting tools used in small businesses.

## 📘 About the Data

Although the café’s POS system is a legacy solution with no API integration, it supports **daily scheduled reports** that output detailed end-of-day sales. These reports have been collected since the reopening of Renago’s Caffe after COVID-19. The files reflect item-level sales transactions for drinks, food, and modifiers.

The reporting system used was designed in the early 2000s with **print-first formatting** in mind. As a result, the reports include:
- Hard-coded **subtotals** for each date  
- Multiple **header rows**  
- Visual formatting that requires transformation to convert into a clean, tabular form

These quirks provide an excellent teaching opportunity for learning **Power Query Editor (PQE)**, where users will reshape and clean the dataset before uploading it to Power BI.

## 📊 Sample Transformation Task

Your first hands-on task will involve loading one of these files and filtering for the total number of *Latte (Hot)* drinks sold in the year 2022. You’ll begin by removing headers, deleting subtotal rows, and shaping the data into a usable table—just like professionals do.

## 📄 Data Dictionary

| Column Name     | Description |
|------------------|-------------|
| `ITEM#`          | Unique ID assigned to each product sold |
| `ITEM NAME`      | Full product name, including temperature (e.g., "Americano (Iced)") |
| `REG#`           | Register number where the transaction occurred |
| `DEPT`           | Internal department code for categorization |
| `SIZE`           | Size of the item sold (e.g., MD = Medium, LG = Large) |
| `QTY`            | Quantity sold. Negative numbers represent refunds or cancellations |
| `PRICE`          | Unit price of the item sold |
| `TOTAL`          | `QTY * PRICE`, before modifiers or containers |
| `MODIFIERS`      | Extra charges for customizations (e.g., syrup, extra shot) |
| `CONTAINER`      | Cost added if item is served to-go (e.g., croissant in a box) |
| `GRAND TOTAL`    | Final sale amount after all adjustments |
