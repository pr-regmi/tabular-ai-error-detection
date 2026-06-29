# Medium Complexity Dataset Notes

## Objective

Create a controlled tabular dataset to evaluate AI-based error detection under increased structural complexity.

## Dataset Configuration

Complexity Level: Medium

Rows: 100

Dependency Level: 5

Columns:

* OrderID
* CustomerType
* Quantity
* Price
* Discount
* TaxRate
* Tax
* Subtotal
* Total
* AmountPaid

Relationships:

1. Subtotal = Quantity × Price

2. If Discount > 0:
   Subtotal = Subtotal × (1 − Discount)

3. Tax = Subtotal × TaxRate

4. Total = Subtotal + Tax

5. AmountPaid = Total

Error Rate:

* Missing Values: 10%
* Formula Errors / Inconsistent Values: 10%

## Dataset Files

medium_complex.csv → clean reference dataset (no injected errors)

medium_complex_test.csv → dataset containing injected errors

medium_complex_errors.csv → ground truth labels

## Error Injection Strategy

Inject 20 total errors:

Missing Values (10)

Formula Errors / Inconsistent Values (10)

Missing values may be introduced in input columns.

Formula errors may be introduced in:

* Discount
* Tax
* Subtotal
* Total
* AmountPaid

Errors will be distributed across separate rows.

## Ground Truth Definition

Ground truth records:

* row index
* affected column
* error category

Ground truth stores error labels only and does not store corrected values.

## Evaluation Plan

Future evaluation will compare AI predictions against ground truth using:

* Precision
* Recall
* F1 Score
