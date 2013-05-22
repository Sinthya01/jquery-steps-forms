|Settings name|Description|Type|Default value|
|---|---|---|---|


```javascript
var settings = {
    /**
     * HTML & CSS Configuration
     **/
        
    /**
     * The header tag is used to find the step button text within the declared wizard area.
     **/
    headerTag: "h1",
    /**
     * The body tag is used to find the step content within the declared wizard area.
     **/
    bodyTag: "div",
    /**
     * The content container tag which will be used to wrap all step contents.
     **/
    contentContainerTag: "div",
    /**
     * The action container tag which will be used to wrap the pagination navigation.
     **/
    actionContainerTag: "div",
    /**
     * The steps container tag which will be used to wrap the steps navigation.
     **/
    stepsContainerTag: "div",
    /**
     * The css class which will be added to the outer component wrapper.
     **/
    cssClass: "wizard",

    /*
     * Tempplates
     */

    /**
     * The title template which will be used to create a step button.
     **/
    titleTemplate: "<span class='number'>#index#.</span> #title#",
    /**
     * The loading template which will be used to create the loading animation.
     **/
    loadingTemplate: "<span class='spinner'></span> #text#",

    /*
     * Behaviour
     */

    /**
     * Sets the focus to the first wizard instance in order to enable the key navigation from the begining if `true`. 
     **/
    autoFocus: false,
    /**
     * Enables all steps from the begining if `true` (all steps are clickable).
     **/
    enableAllSteps: false,
    /**
     * Enables keyboard navigation if `true` (arrow left and arrow right).
     **/
    enableKeyNavigation: true,
    /**
     * Enables pagination if `true`.
     **/
    enablePagination: true,
    /**
     * Suppresses pagination if a form field is focused.
     **/
    suppressPaginationOnFocus: true,
    /**
     * Enables cache for async loaded or iframe embedded content.
     **/
    enableContentCache: true,
    /**
     * Shows the finish button if enabled.
     **/
    enableFinishButton: true,
    /**
     * Not yet implemented.
     **/
    preloadContent: false,
    /**
     * Shows the finish always (on each step; right beside the next button) if `true`. 
     * Otherwise the next button will be replaced by the finish on the last step.
     **/
    showFinishButtonAlways: false,
    /**
     * Forces forward navigation (move backward is not possible).
     **/
    forceMoveForward: false,
    /**
     * Saves the current state (step position) to a cookie.
     * By coming next time the last active step becomes activated.
     **/
    saveState: false,
    /**
     * The position to start on (zero-based).
     **/
    startIndex: 0,

    /*
     * Animation Effect Configuration
     */

    /**
     * The animation effect which will be used for step transitions.
     **/
    transitionEffect: $.fn.steps.transitionEffect.none,
    /**
     * Animation speed for step transitions (in milliseconds).
     **/
    transitionEffectSpeed: 200,

    /*
     * Events
     */

    /**
     * Fires before the step changes and can be used to prevent step changing by returning `false`. 
     * Very useful for form validation. 
     **/
    onStepChanging: function (event, currentIndex, newIndex) { return true; },
    /**
     * Fires after the step has change. 
     **/
    onStepChanged: function (event, currentIndex, priorIndex) { },
    /**
     * Fires before finishing and can be used to prevent completion by returning `false`. 
     * Very useful for form validation.
     **/
    onFinishing: function (event, currentIndex) { return true; }, 
    /**
     * Fires after completion. 
     **/
    onFinished: function (event, currentIndex) { },

    /*
     * Labels
     */

    labels: {
        /**
         * This label is important for accessability reasons. 
         * Indicates which step is activated.
         **/
        current: "current step:",
        /**
         * Label for the finish button.
         **/
        finish: "Finish",
        /**
         * Label for the next button.
         **/
        next: "Next",
        /**
         * Label for the previous button.
         **/
        previous: "Previous",
        /**
         * Label for the loading animation.
         **/
        loading: "Loading ..."
    }
};
```