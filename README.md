# Evaluating the Impact of Structural Complexity on AI-Based Error Detection in Tabular Data

## Research Question
How does increasing structural complexity in tabular datasets affect the precision and recall of AI-based error detection systems?

## Project Objective
The goal of this project is to study how increasing complexity in tabular datasets affects the ability of AI systems to detect errors. The study focuses on relational dependencies and missing or inconsistent values and evaluates performance using precision and recall.

## Methodology

### Dataset Generation
Create synthetic tabular datasets with increasing levels of structural complexity.

### Error Injection
Introduce controlled errors including:
- Missing values
- Calculation errors
- Logical inconsistencies

### AI Evaluation
Apply the same AI evaluation process across all datasets and compare performance.

### Metrics
- Precision
- Recall
- F1 Score

## Complexity Levels

| Level | Dependencies | Missing | Inconsistent |
|---|---:|---:|---:|
| Low | 1 | 5% | 5% |
| Medium | 3 | 10% | 10% |
| High | 5 | 15% | 15% |

## Current Progress

- [x] Created repository and project setup  
- [x] Design synthetic datasets  
- [ x] Introduce controlled errors  
- [ ] Evaluate AI performance  
- [ ] Calculate precision, recall, and F1-score  
- [ ] Analyze findings  
- [ ] Complete final report  

## Planned Repository Structure

datasets/  
ground_truth/  
prompts/  
results/  
figures/  
report/  
notes/

## Expected Outcome

This project aims to understand whether increasing structural complexity reduces AI performance in detecting errors in tabular datasets and identify which types of errors become more difficult to detect. The findings may provide insights into the limitations of AI and LLM-based systems and highlight the importance of data quality and validation in financial and business decision-making environments.
