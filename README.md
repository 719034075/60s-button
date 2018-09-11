# 60s-button

> a 60s'button using localStorage

## functions

+ remainTime()
+ changeButtonState()
+ timeEvent()
+ entry()

### remainTime

Calculate the remaining time.

If the storage `start-time` is not populated, it will return 60s and create the storage `start-time`.

Else, it will return the remaining time.

### changeButtonState

Change the button's state.

If the remaining time equal or less than 0s, it will change the button's value, disable state.Of course, it will remove
the storage `start-time` and the cron job.

Else, it will change the button's value about the remaining time and be sure that the button's state is disabled.

### timeEvent

Change the state of the button once every second.

### entry

Every time you open the page(maybe you refresh the page),it will check the storage `start-time`.

If the storage `start-time` is not populated, it will bind the function `timeEvent` on the button.

Else, run the function `timeEvent` automatically.
