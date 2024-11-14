# Front End Validation

Form validation has to happen in most systems. Because I got tired of writing piecemeal validation libraries that didn't suit all of my needs for every project I decided to build this validation library for flexible use across multiple projects.

## Validation Lifecycle

The following is the lifecycle of the validation library.

1) Page with input element(s) is loaded.
2) Validation is attached to input element(s).
3) Optionally, an initial validation takes place against every input element and initial validation messages are generated and outputted to a default or user defined location.
4) Validation is triggered on an input element (and any related input element(s)) as the user inputs data into the form fields. This is debounced by default to provide feedback that is fast but not instant.
5) When a submission event occurs a final validation check is performed and input element(s) and any resulting validation messages are shown in their errored form.

## Required in Code

* A validation status for each individual check must be stored on the input element so that validation for all of the checks can pass or fail on that element.
* Validation messages should be produced in such a way that the end user can choose a location to place them.
* Should be agnostic to any CSS framework.

## Wishlist

* Adding basic validation to a page is as simple as including the script.
* Adding advanced validation to a page is as simple as creating a configuration object on the page.
* Configuration for debouncing time.
* Custom validations can be defined in form submission.
* Configuration option for showing all or a single number of validation messages.