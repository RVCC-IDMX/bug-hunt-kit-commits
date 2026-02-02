# Bug 2: The grade that's never excellent

## Trace table

| Step | score | Condition checked | Result |
| ---- | ----- | ----------------- | ------ |
|   1   |    95   |         >=65          |    D    |
|   2   |     95  |           N/A        |     D   |
|   3  |      95  |           N/A        |     D   |

## What's wrong

There is a logic order bug. 

## Fixed pseudocode

```pseudo

BEGIN
    DISPLAY "Enter your score (0-100):"
    INPUT score

    IF score >= 90 THEN
        DISPLAY "Grade: A - Excellent"
    ELSEIF score >= 80 THEN
        DISPLAY "Grade: B - Good"
    ELSEIF score >= 70 THEN
        DISPLAY "Grade: C - Satisfactory"
    ELSEIF score >= 60 THEN
        DISPLAY "Grade: D - Passing"
    ELSE
        DISPLAY "Grade: F - Failing"
    ENDIF
END

```

## Reframed explanation

Explain this bug as if it existed in a domain you care about (gaming ranks, recipe measurements, fitness tracking, music playlists, etc.). What system would break, and how?

The conditions are checked top to bottom, which is why it sticks at "if score >=60, Grade D". It would not update to a player's current stats. 

## Flowchart

Download your fixed flowchart and save it as `flowcharts/bug2-fixed.svg`
