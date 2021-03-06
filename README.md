# ember-pick-time

This is an Ember addon that uses the wonderful [ember-power-select](https://github.com/cibernox/ember-power-select) component for allowing the user to select a time [am / pm] from a picklist.

## Installation

Ember Time Picker has the same requirements as ember-power-select. Hence, we need to install [ember-power-select](https://github.com/cibernox/ember-power-select) as well.
This is an ember-cli addon so this will install the addon:
```
ember install ember-pick-time
```
## Example #1

Following is basic example with selected and disabled proporty.

```handlebars
    {{ember-pick-time
        selected = selectedTime
        disabled=false
    }}
```

## Example #2

Following is extended example with two timepickers. This is to handle "From Time" and "To time".

```handlebars
    From Time
    {{ember-pick-time
        selected = fromTime
    }}
    To Time
    {{ember-pick-time
        selected = toTime
        startTime = fromTime // Ex, '7:00 PM' or '12:15 AM'
        disabled = false // optional
    }}
```

## Attributes

| attribute | Type | Description |
| --- | --- | --- |
| selected | Required | The selected option |
| startTime | optional | This will the time from which user want to display time-list |
| disabled | `boolean` | Default it's `false`. When truthy the component cannot be interacted |