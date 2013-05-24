**A: It is quite easy just add three additional lines of code to the `onStepChanging` event. See code example below.**

```javascript
$("#wizard").steps({
    onStepChanging: function (event, currentIndex, newIndex)
    {
        // Allways allow step back to the previous step even if the current step is not valid!
        if (currentIndex > newIndex)
        {
            return true;
        }

        ...
    }
});
```