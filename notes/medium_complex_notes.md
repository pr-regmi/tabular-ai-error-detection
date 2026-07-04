# Medium Complexity Dataset Notes

## Objective

Create a controlled tabular dataset to evaluate AI-based error detection under increased structural complexity.

## Dataset Configuration

Complexity Level: Medium

Rows: 100

Dependency Level: 5

Relationships:

* Subtotal = Quantity × Price
* If Discount > 0, Subtotal = Subtotal × (1 − Discount)
* Tax = Subtotal × TaxRate
* Total = Subtotal + Tax
* AmountPaid = Total

Error Rate:

* Missing Values: 10%
* Inconsistent / Formula Errors: 10%

## Dataset Files

medium_complex.csv → clean reference dataset (no injected errors)

medium_complex_test.csv → dataset containing injected errors

medium_complex_errors.csv → ground truth labels

## Error Injection Strategy

Injected 20 total errors.

Missing Values (10)

* Missing values will be introduced in input columns such as Quantity, Price, Discount, and TaxRate.

Formula / Inconsistent Errors (10)

* Formula errors will be introduced in calculated columns such as Subtotal, Tax, Total, and AmountPaid.
* Some rows may contain more than one error to better represent real-world data quality issues.

## Ground Truth Definition

Ground truth records:

* row index
* affected column
* error category

Ground truth stores error labels only and does not store corrected values.

## Evaluation Plan

AI predictions will be compared against the ground truth using:

* Precision
* Recall
* F1 Score

The results will be compared with the Low Complexity dataset to examine how increasing structural complexity affects AI-based error detection.
