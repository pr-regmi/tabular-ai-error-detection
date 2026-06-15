# Dataset V1 (Final)

## Dataset Type

Sales Transactions

## Columns

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

## Dependencies

1. Subtotal = Quantity × Price

2. If CustomerType = VIP:
   Discount = 10% × Subtotal

3. Tax = (Subtotal − Discount) × TaxRate

4. Total = Subtotal − Discount + Tax

5. AmountPaid = Total

## Complexity Levels

### Low

* Use Dependency 1 only
* 5% missing/inconsistent values

### Medium

* Use Dependencies 1–3
* 10% missing/inconsistent values

### High

* Use Dependencies 1–5
* 15% missing/inconsistent values

## Error Types

* Missing values
* Formula errors
* Logical inconsistencies

## Evaluation Metrics

* Precision
* Recall
* F1-score
