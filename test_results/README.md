# GPT-4 Regression Analysis Project

## Overview
This project documents and analyzes the regression in GPT-4's performance after the March 2024 update. The analysis covers multiple aspects of AI behavior including technical competence, expert-level reasoning, emotional intelligence, and response to user emotions.

## Key Findings
- Average regression rate across all test categories: 33%
- Individual category regression rates:
- Technical/Base: 34%
- Expert-level: 38%
- Emotional: 28%
- User Emotion Effect: 32%

Despite the limited sample size (200 total tests, 50 per category), the consistency of regression across different testing methodologies and scenarios suggests a significant and observable degradation in system performance.

### Statistical Significance Analysis
While the sample size (200 tests) is at the lower bound for statistical significance, several factors support the reliability of our findings:

The most intriguing finding is that the degradation indicators in formal smoke tests (~33%) almost exactly match the results from less formalized testing approaches.

There are two possible interpretations:
1. This could be a coincidence due to the small sample size (200 tests total)
2. This could reflect the actual system degradation level

Considering:
- The stability of observed patterns
- Consistency across different testing methodologies
- Correlation with user subjective assessments
- Reproducibility across different scenarios

We lean towards the second interpretation: the matching results likely indicate that we are measuring the actual system degradation level rather than random fluctuations. This significantly increases the reliability of our conclusions despite the limited sample size.

## Project Structure

### Core Documentation
- GPT4o_Functional_Regression_Summary.md - Primary summary document containing test results and analysis
- TestCases/ - Directory containing test cases and examples
  - EmotionalTests.md - Emotional intelligence and tone analysis tests
  - ExpertTests.md - Expert-level reasoning and complex problem-solving tests
  - TechnicalTests.md - Basic technical competency tests
  - UserEmotionTests.md - Tests for response to user emotional states

### Test Results
- Results/ - Directory containing detailed test results and analysis
  - DetailedAnalysis.md - In-depth analysis of test results
  - RegressionPatterns.md - Identified patterns in performance degradation

## Observations

### Key Points
1. **Consistent Degradation**: The regression is observable across all test categories
2. **User Impact**: The degradation level is sufficient to create noticeable user discomfort
3. **Pattern Reliability**: Despite limited sample size, the consistency of results across different testing methodologies strengthens the findings

### Methodology Notes
- Tests were conducted using a mix of structured and semi-structured approaches
- Results show consistent degradation patterns regardless of testing methodology
- The similarity in results between different testing approaches supports the validity of findings

## Implications
The findings suggest a significant regression in GPT-4's capabilities that affects both technical and interpersonal aspects of its performance. The consistency of these findings across different testing methodologies indicates a systemic rather than isolated issue.