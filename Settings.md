## Appearance

|Setting Name|Description|Type|Default Value|
|---|---|---|---|
|headerTag|The header tag is used to find the step button text within the declared wizard area.|String|`h1`|
|bodyTag|The body tag is used to find the step content within the declared wizard area.|String|`div`|
|contentContainerTag|The content container tag which will be used to wrap all step contents.|String|`div`|
|actionContainerTag|The action container tag which will be used to wrap the pagination navigation.|String|`div`|
|stepsContainerTag|The steps container tag which will be used to wrap the steps navigation.|String|`div`|
|cssClass|The css class which will be added to the outer component wrapper.|String|`wizard`|
|[stepsOrientation](https://github.com/rstaib/jquery-steps/wiki/Steps-Orientation)|Determines whether the steps are vertically or horizontally oriented.|String or Integer|`horizontal` or `0`|

## Templates

|Setting Name|Description|Type|Default Value|
|---|---|---|---|
|titleTemplate|The title template which will be used to create a step button.|String|`<span class="number">#index#.</span> #title#`|
|loadingTemplate|The loading template which will be used to create the loading animation.|String|`<span class="spinner"></span> #text#`|

## Behaviour

|Setting Name|Description|Type|Default Value|
|---|---|---|---|
|autoFocus|Sets the focus to the first wizard instance in order to enable the key navigation from the begining if `true`.|Boolean|`false`|
|enableAllSteps|Enables all steps from the begining if `true` (all steps are clickable).|Boolean|`false`|
|enableKeyNavigation|Enables keyboard navigation if `true` (arrow left and arrow right).|Boolean|`true`|
|enablePagination|Enables pagination (next, previous and finish button) if `true`.|Boolean|`true`|
|suppressPaginationOnFocus|Suppresses pagination if a form field is focused.|Boolean|`true`|
|enableContentCache|Enables cache for async loaded or iframe embedded content.|Boolean|`true`|
|enableFinishButton|Shows the finish button if enabled.|Boolean|`true`|
|showFinishButtonAlways|Shows the finish button always (on each step; right beside the next button) if `true`. Otherwise the next button will be replaced by the finish button if the last step becomes active.|Boolean|`false`|
|forceMoveForward|Prevents jumping to a previous step.|Boolean|`false`|
|saveState|Saves the current state (step position) to a cookie. By coming next time the last active step becomes activated.|Boolean|`false`|
|startIndex|The position to start on (zero-based).|Integer|`0`|

## Transition Effects

|Setting Name|Description|Type|Default Value|
|---|---|---|---|
|[transitionEffect](https://github.com/rstaib/jquery-steps/wiki/Transition-Effects)|The animation effect which will be used for step transitions.|String or Integer|`none` or `0`|
|transitionEffectSpeed|Animation speed for step transitions (in milliseconds).|Integer|`200`|

## Events

|Setting Name|Description|Type|Default Value|
|---|---|---|---|
|onStepChanging|Fires before the step changes and can be used to prevent step changing by returning `false`. Very useful for form validation.|Event|`function (event, currentIndex, newIndex) { return true; }`|
|onStepChanged|Fires after the step has change.|Event|`function (event, currentIndex, priorIndex) { }`|
|onFinishing|Fires before finishing and can be used to prevent completion by returning `false`. Very useful for form validation.|Event|`function (event, currentIndex) { return true; }`|
|onFinished|Fires after completion.|Event|`function (event, currentIndex) { }`|

## Labels

|Setting Name|Description|Type|Default Value|
|---|---|---|---|
|current|This label is important for accessability reasons. Indicates which step is activated.|String|`current step:`|
|pagination|This label is important for accessability reasons and describes the kind of navigation.|String|`Pagination`|
|finish|Label for the finish button.|String|`Finish`|
|next|Label for the next button.|String|`Next`|
|previous|Label for the previous button.|String|`Previous`|
|loading|Label for the loading animation.|String|`Loading ...`|

## Example

```javascript
var settings = {
    /* Appearance */
    headerTag: "h1",
    bodyTag: "div",
    contentContainerTag: "div",
    actionContainerTag: "div",
    stepsContainerTag: "div",
    cssClass: "wizard",
    stepsOrientation: $.fn.steps.stepsOrientation.horizontal,

    /* Templates */
    titleTemplate: '<span class="number">#index#.</span> #title#',
    loadingTemplate: '<span class="spinner"></span> #text#',

    /* Behaviour */
    autoFocus: false,
    enableAllSteps: false,
    enableKeyNavigation: true,
    enablePagination: true,
    suppressPaginationOnFocus: true,
    enableContentCache: true,
    enableFinishButton: true,
    preloadContent: false,
    showFinishButtonAlways: false,
    forceMoveForward: false,
    saveState: false,
    startIndex: 0,

    /* Transition Effects */
    transitionEffect: $.fn.steps.transitionEffect.none,
    transitionEffectSpeed: 200,

    /* Events */
    onStepChanging: function (event, currentIndex, newIndex) { return true; },
    onStepChanged: function (event, currentIndex, priorIndex) { },
    onFinishing: function (event, currentIndex) { return true; }, 
    onFinished: function (event, currentIndex) { },

    /* Labels */
    labels: {
        current: "current step:",
        pagination: "Pagination",
        finish: "Finish",
        next: "Next",
        previous: "Previous",
        loading: "Loading ..."
    }
};
```