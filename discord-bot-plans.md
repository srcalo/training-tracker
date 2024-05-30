# Workout bot features

## Check in system

Set frequency goal for the week

Include weekly streak system

### Commands

1. /check-in

    If weekly goal set, display goal progress and congratulations if goal achieved. If goal isn't set, let them know that they can set a goal with `/set-weekly-goal. Record last check-in date

    Remind user they can log their exercise using /log new-entry

2. /set-weekly-goal
3. /streak

    Display both current weekly streak and highscore. If no goal set, display goal must be set with /set-weekly-goal.

## Logging system

Can log exercise, bodyweight, calories

Logs weight, time, reps, sets, date entered

### Commands

1. /log new-entry
    - Options:
        - exercise
        - body weight
        - calories
2. /log view
    - Display all possible values for selection
    - After selection, display current PB and historical graph
    - Graph will need to check for what type of exercise to determine axis
    - Exercise axis: x=date, y=weight/time/pace, color=reps

## Data Objects

1. UserData:

    - Key: userID
    - Values:
        - logObject
        - weeklyGoal
        - currentStreak
        - highestStreak
        - lastCheckInDate

2. Log Object

    - Key: exercise
    - Value:
        - List of Entry Object

3. Entry Object
    - Name
    - Date: default=currentDate
    - Weight
    - Reps
    - Sets
    - Duration
    - Distance

### Notes

Autocomplete Name with all keys in LogObject for user

Prepopulate user LogObject with Calorie key and Bodyweight Key

Bodyweight and Calories both use Weight for their value
