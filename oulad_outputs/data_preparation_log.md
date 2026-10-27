# OULAD data preparation log

## Date

The notebook was prepared during August 2026.

## Files loaded

The analysis used the assessments, studentAssessment, studentInfo, studentRegistration, vle and studentVle tables. The studentVle table was read from split CSV files and recombined vertically.

## Preparation decisions

1. Raw source files were read without overwriting them.
2. Column names were stripped of accidental surrounding spaces.
3. Duplicate rows, duplicate keys, missing values and unmatched relationships were checked before merging.
4. Pass and Distinction were coded as 1. Fail and Withdrawn were coded as 0.
5. Examination records were excluded from early assessment predictors.
6. Assessment score missingness was retained and represented with missingness indicators.
7. Engagement count features were filled with zero after merging because no interaction record represents no recorded activity for that feature.
8. Separate cumulative prediction windows were created at weeks 2, 4 and 6 using day cutoffs of 14, 28 and 42.
9. Negative-date VLE records were reported and retained because they represent activity before the official course start date.
10. date_unregistration was excluded from predictors because it may reveal a later withdrawal event.

## Preliminary status

The datasets and audit tables were created for preliminary analysis. Model training, hyperparameter tuning, SMOTE and final evaluation metrics are not completed in this preparation stage.
