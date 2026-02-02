# Bug 3: The infinite greeting

## Trace table

| Step | usersGreeted | usersGreeted < 3 | Action |
| ---- | ------------ | ---------------- | ------ |
|   1   |       0       |         0         |     Display   |
|   2   |       0      |          0       |    Display    |
|   3   |       0      |          0        |    Display    |
|   4   |       0       |         0         |    Display    |

## What's wrong

There is an infinate loop bug.

## Fixed pseudocode

```pseudo

// Fixed: counter is updated each loop iteration

BEGIN
    SET usersGreeted TO 0

    WHILE usersGreeted < 3 DO
        DISPLAY "What is your name?"
        INPUT userName
        DISPLAY "Hello, " + userName + "!"

        SET usersGreeted TO usersGreeted + 1
    END WHILE

    DISPLAY "All users have been greeted!"
END

```

## Warning for future students

Write a 3-4 sentence warning that would help a future student avoid this type of bug. What should they always check before saying their loop is finished?

The before code results in an infinite loop. Make sure to increment the usersGreeted. This will update the loop iteration. 

For fun, you may choose the voice of your warning: HAP, Grace, Prof. Teeters, or a character of your choosing. Feel free to have an AI assistant help with this.

**Voice chosen:**

**Used AI assistant (yes/no):**

No

## Flowchart

Download your fixed flowchart and save it as `flowcharts/bug3-fixed.svg`
