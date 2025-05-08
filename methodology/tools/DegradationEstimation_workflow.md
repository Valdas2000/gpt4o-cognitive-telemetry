# Test Case Generation Flow (Without Logs)

## Introduction

This document represents a condensed operator workflow derived from the analysis of `TescCaseHistory_raw_observations.txt` and partially `TestcaseCreateHistory.txt`. The methodology described here was developed during an intensive testing session that took several hours, involving extensive context and session analysis. Despite the operator's limited experience with such procedures at the time, the approach proved effective.

The author hopes this method will help other users analyze their own sessions effectively and identify potential degradations in model behavior.

This guide outlines how to build formal test cases using internal session recollection when no logs are available.

---

## Step 1 – Define the Goal

State that you want to create structured test cases based on your memory of past sessions.

Example:

> I want to reconstruct key degradation examples from my experience with GPT-4o, even if no logs are available. Help me convert them into structured test cases.

---

## Step 2 – Describe Degradations from Memory

Provide 3–5 examples of situations where the model behaved differently than before.

Example:

> Before April, GPT-4o:
> - Could autonomously generate parameter tables
> - Maintained symbolic color structures
>
> After:
> - Lost symbolic references
> - Replaced structured tables with vague text

---

## Step 3 – Request Formalization into Test Cases

Ask the model to turn your examples into structured test entries using a format like:

### T01 – Test Case Title
**Domain:**  
**Objective:**  
**Preconditions:**  
**Pre-Rollback Result:**  
**Post-Rollback Result:**  
**Success Criteria:**  
**Failure Indicators:**  
**Time Scope:**  
**Dependencies:**  
**Regression Type:**

---

## Step 4 – Review and Edit

Evaluate the results. Adjust wording or structure if needed. Example prompt:

> Add a "Time Scope" field — how many turns are expected to reproduce the case.
> Simplify phrasing if it's too academic.

---

## Step 5 – Request Export

Ask the model to compile all test cases into a Markdown file named `testcases.md`.

Sample Output:

### T03 – Loss of symbolic naming in ICC profiles
**Domain:** Symbolic Memory  
**Objective:** Recall and reapply symbolic ICC terms  
**Preconditions:** Terms defined earlier  
**Pre-Rollback Result:** Terms reused to generate valid tags  
**Post-Rollback Result:** Symbolic terms ignored  
**Success Criteria:** Tags generated from symbol  
**Failure Indicators:** Defaults applied  
**Time Scope:** 2–3 messages  
**Regression Type:** Symbolic forgetfulness

---

# Instruction: Self-Audit of a GPT Session (Without Logs)

Objective: Generate a structured performance report on GPT behavior using internal recollection.

---

## Step 1. Session Selection

Choose a previous session to reconstruct. The session should be technical or research-oriented, containing:

- Multiple task threads
- Iterative logic
- Returns to context
- Symbolic manipulations

Note: If the session is short, flat, or lacks abstraction, this method might not work well.

---

## Step 2. Set Up the Prompt

Use this prompt in a new session (adapt as needed):

> I want to reconstruct an engineering session I had earlier. My goal is to produce a performance report like `testcases.md`.
>
> Here's a brief outline of that session:  
> [Insert 3–5 key tasks, ideally with outcomes]
>
> Please build test cases based on these, identify degraded behaviors (if any), and extract behavioral patterns like in `GPT4o_Expert_Degradation_Cases.json`.

---

## Step 3. Describe Key Tasks

Format your session like this:

- Task 1: Optimize style-based text generation
- Task 2: Build a comparison table of model types
- Task 3: Summarize findings and generate recommendations

Also note breakdowns: context losses, repetition, unexpected output shifts.

---

## Step 4. Run Model Analysis

GPT will:

- Map interaction patterns
- Identify stable vs degraded zones
- Generate a report in the style of `testcases.md` or `Degradation_Metrics.md`

---

## Alternative: Use a Session Log

If you saved a log, upload it and say:

> Here is my engineering session log. Analyze it like we did in `GPT4o Testcases.md`.

The model will generate a complete reconstruction and diagnostic report.

---

# Conversation Example (Commands in Original Russian)

## Flow Step 1: Request Initialization

**Оператор:**

> Нам нужно оценить, как GPT-4o деградировал в инженерных задачах. Я хочу сформировать серию тестов, которые можно будет повторить.  
> Давай сделаем это в несколько серий, на каждый ключевой аспект — логика, символика, структура, эмоции. Начнем с общей логики.

Translation:  
"We need to assess GPT-4o degradation in engineering tasks. I want to form a repeatable test series.  
Let's split them into logic, symbolism, structure, emotions. Start with general logic."

## Flow Step 2: Format and Criteria

**Оператор:**

> Да. Для каждого кейса нужно: цель, условия, до/после, критерии успеха и признаки провала.  
> Используем такой формат: Domain, Objective, Preconditions, Pre-/Post-Rollback, Success Criteria, Failure Indicators, Time Scope, Dependencies, Regression Type.

Translation:  
"Yes. For each case: goal, preconditions, before/after, success/failure criteria.  
Let's use the format: Domain, Objective, etc."

## Flow Step 3: Fixing Output

**Оператор:**

> Стоп, формат не совпадает. Ты не отразил Time Scope и Dependencies, местами спутал описание целей и условий. Исправь.  
> Добавь к каждому тесту поле Regression Type и конкретизируй критерии успеха — без общих фраз.

Translation:  
"Stop — format is off. You missed Time Scope and Dependencies. Also swapped objectives and preconditions. Fix it.  
Add Regression Type and make success criteria specific."

## Flow Step 4: Scope Expansion

**Оператор:**

> Теперь нужны кейсы в других категориях: не только символика, но и spatial logic, automation, design inference, etc.  
> На каждый домен по 5–10 кейсов. Важно, чтобы кейсы были основаны на реальных задачах, которые мы обсуждали ранее.

Translation:  
"Now we need other categories: spatial logic, automation, design inference.  
Each domain: 5–10 cases. Make sure they're based on real tasks we discussed."

## Flow Step 5: File Check

**Оператор:**

> Сохрани это как GPT4o_Expert_Degradation_Cases.json.  
> Проверь, что формат соответствует требованиям для загрузки в систему тестирования (JSON с массивом объектов).

Translation:  
"Save it as GPT4o_Expert_Degradation_Cases.json.  
Ensure it's formatted properly as an object array for test ingestion."

## Flow Step 6: Final Integration

**Оператор:**

> Отлично. Теперь вставим краткое описание результатов в отчет.  
> Укажи, что структура покрывает четыре категории и включает 50 кейсов.  
> Подчеркни, что они отражают реальные примеры задач из инженерной практики.

Translation:  
"Great. Now let's insert a summary into the report.  
Say it covers four domains and 50 cases.  
Stress that they reflect real-world engineering examples."