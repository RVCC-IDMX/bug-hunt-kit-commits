# Bug 1: The counter that counts wrong

## Trace table

| Step | counter | counter < 5 | Action |
| ---- | ------- | ----------- | ------ |
|   1   |    1     |      1       |   1+1     |
|   2   |    2     |      2       |   2+1     |
|   3   |    3     |      3       |   3+1     |
|   4   |    4     |      4       |   4+1     |
|      |         |             |        |
|      |         |             |        |

## What's wrong

When the counter becomes 5, the condition counter <5 is false, the loop stops

## Fixed pseudocode

```pseudo

BEGIN
    SET counter TO 1

    WHILE counter <= 5 DO
        DISPLAY "Count: " + counter
        SET counter TO counter + 1
    END WHILE

    DISPLAY "Done counting to 5!"
END


```

## Real-world consequences

Imagine this bug existed in a real system. In 2-3 sentences, describe what could go wrong.

The code would stop before hitting 5. There would be no logical end point. 

## Flowchart

Download your fixed flowchart and save it as `flowcharts/bug1-fixed.svg`
