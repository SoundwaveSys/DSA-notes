# Flowchart Problem-Solving Lab

A programming language can express a solution, but it cannot repair flawed logic. In this lab, we use the ideas from the previous lessons i.e. inputs, outputs, constraints, sequence, selection, iteration, and pseudocode to solve problems before writing language-specific code.

Follow the same cycle each time:

**Understand → Model → Draw → Dry-run → Challenge → Express as pseudocode**

The worked examples follow the video’s order: student results, largest values, grades, sums, and digits. The restaurant, free-delivery, and slab-billing exercises from the learning notes follow as further applications. All eight problems from the notes are included.

------------------------------------------------------------------------

## Before drawing: answer seven questions

1. What is the problem asking in one sentence?
2. What inputs are available?
3. What output is required?
4. Which calculations are necessary?
5. Which conditions create different paths?
6. Which actions repeat?
7. Which boundaries or invalid cases must be considered?

Only then choose the shapes. A flowchart records executable reasoning, not the order in which ideas happened to occur.

------------------------------------------------------------------------

## 1. Student result with a subject-wise rule

### Requirement

Read marks in three subjects. Marks must lie from 0 to 100. Display “Invalid marks” if any input is outside that range. Otherwise, display the average and report Pass only when every subject has at least 40 marks.

### Decompose the problem

1. Validate all inputs.
2. If valid, calculate the average.
3. Check the subject-wise pass rule.
4. Display the result.

### Why validation comes first

For marks `90, 105, 80`, calculating an average gives a number, but that number has no valid meaning under the stated system because 105 is outside the allowed range.

### Flowchart

![Three Subject Results](https://static.takeuforward.org/content/flowchart-problem-solving-lab-images/01-three-subject-result.png)

**Three Subject Results**

### Dry runs

### Case A: `70, 80, 90`

All values are valid. Average is 80. Every mark is at least 40. Result: Pass.

### Case B: `90, 90, 30`

All values are valid. Average is 70. One subject is below 40. Result: Fail.

### Case C: `90, 105, 80`

One mark exceeds 100. Result: Invalid marks. Average and pass status should not be reported.

### Pseudocode

```text
READ m1, m2, m3

IF m1 < 0 OR m1 > 100 OR
   m2 < 0 OR m2 > 100 OR
   m3 < 0 OR m3 > 100
    DISPLAY "Invalid marks"
    STOP
END IF

SET average = (m1 + m2 + m3) / 3

IF m1 >= 40 AND m2 >= 40 AND m3 >= 40
    DISPLAY average, "Pass"
ELSE
    DISPLAY average, "Fail"
END IF