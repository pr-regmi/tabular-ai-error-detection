# Low Complexity Dataset Notes

## Objective

Create a controlled tabular dataset to evaluate AI-based error detection.

## Dataset Configuration

* Complexity Level: Low
* Rows: 100
* Dependency Level: 1 Dependency Level: 1
(One relationship is evaluated as : Subtotal = Quantity × Price)
* Error Rate: 5%

## Dataset Files

* low_complex.csv → clean reference dataset ( no injected errors)
* low_complex_test.csv → dataset containing injected errors
* low_complex_errors.csv → ground truth labels

## Error Injection Strategy

Injected 5 total errors:

### Missing Values (2)

* Row 10 → Quantity
* Row 51 → Price

### Formula Errors (3)

* Row 42 → Subtotal
* Row 60 → Subtotal
* Row 94 → Subtotal

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
