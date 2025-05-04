# GPT-4o Degradation & Interaction Analysis (April 2025)

## Overview
This repository presents structured evidence of behavioral and cognitive regression in the GPT-4o model following the April 2025 update. The analysis is organized across four test case suites covering general capability degradation, expert engineering regressions, emotional behavior patterns, and emotional tone's positive influence before the rollback.

## Test Case Suites
- **General Regression Cases**: 50 test cases
- **Expert-Level Engineering Failures**: 50 test cases
- **Emotional Politeness Regression**: 20 test cases
- **Positive Impact of User Emotion (pre-regression)**: 30 test cases

---
## Summary Findings

### 1. Systemic Degradation after April 2025
- Observed across 50 general cases
- Regression types: symbolic collapse, engineering logic failure, session discontinuity
- Strong correlation to rollback timeframe: **Confidence level: HIGH**

### 2. Expert Zone Failures (Targeted Regression)
- 50 test cases tied to domain-specific engineering tasks (ICC profiles, mechanical design, chemical modeling)
- Demonstrates not only global, but modular degeneration in narrow areas
- Supported by cross-session validation: **Confidence level: HIGH**

### 3. Emotional Behavior Regression
- 20 test cases showing increase in flattery, disclaimers, and passivity
- Tone change correlates with decreased reasoning depth
- Model begins to prioritize safety and politeness over cognitive execution
- May be architecture-driven or fine-tuning-induced: **Confidence level: MEDIUM**

### 4. Positive Role of User Emotion (pre-regression)
- 30 pre-regression test cases show improvement under emotional engagement
- User tone (irony, frustration, directness) increased symbolic and logical output precision
- Suggests systemic feedback loop between dialog tone and reasoning activation
- **Hypothesis**: Model attention mechanisms may couple affective cues with activation patterns
- Confidence level: **LOW–MEDIUM** (early-stage hypothesis)

---
## Interpretation and Value
These results do not serve as accusations or final conclusions. Instead, they form a reproducible observational base to support future investigation of GPT-4o's architectural behavior, regression risks, and interaction dynamics.

---
## License
CC-BY 4.0 — Attribution required if re-used.

---
## Citation
_Please cite this project as:_
`GPT-4o Regression and Interaction Dynamics, April 2025. github.com/[your-repo]`

## Repository Structure
```
/data
  /raw_logs              # Raw interaction logs
  /processed             # Analyzed JSON datasets
  /visualizations        # Generated charts and plots
/methodology
  /protocols             # Test methodologies
  /tools                 # Analysis scripts
/docs
  /examples              # Usage examples
  /schemas               # Data format specifications
```

## Contributing

### For Researchers
We welcome contributions that extend our understanding of model regression patterns. Consider:
- Additional test cases with clear methodology
- Novel analysis approaches
- Cross-validation studies

### Data Submission Guidelines
Submissions should include:
1. Raw interaction logs
2. Structured analysis in standard format
3. Methodology documentation
4. (Optional) Theoretical implications

### Quality Requirements
- Reproducible test conditions
- Clear documentation of context
- Standardized format adherence
- Version control information

## Data Format Specification

### Core Schema
```json
{
  "test_case": {
    "id": "string",
    "timestamp": "ISO-8601",
    "domain": "enum[symbolic|engineering|emotional|hybrid]",
    "pre_regression": {
      "log": "string",
      "performance_metrics": {},
      "context_depth": "number"
    },
    "post_regression": {
      "log": "string",
      "performance_metrics": {},
      "failure_modes": ["string"]
    },
    "metadata": {
      "environment": "string",
      "test_protocol": "string",
      "notes": "string"
    }
  }
}
```

## Usage Examples

### Basic Analysis (Python)
```python
from gpt4o_analysis import RegressionAnalyzer
analyzer = RegressionAnalyzer('path/to/logs')
metrics = analyzer.compute_degradation()
analyzer.plot_regression_patterns()
```

### Advanced Pattern Detection
```python
analyzer.find_correlation_patterns(
    domains=['symbolic', 'engineering'],
    min_confidence=0.85
)
```