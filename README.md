# SpendWise – Smart Budget Tracker

SpendWise is a personal budgeting web application that helps users set a monthly budget, record expenses, monitor their spending, and see how much money they have remaining.

## Week 6 Improvements

This week, SpendWise was improved from a basic budgeting application into an interactive web application.

The main improvements include:

- Added conditional statements to evaluate different budgeting situations.
- Changed individual expense variables into an array of expense records.
- Added loops to calculate totals and display multiple expense records.
- Added DOM manipulation to update the dashboard directly on the webpage.
- Added event listeners for forms and buttons.
- Added input validation to prevent invalid information.
- Added the ability to delete individual expenses.
- Added a Clear All button to remove all expenses.
- Added budget status messages based on spending.
- Added a dynamic progress bar to show budget usage.
- Added expense categories and dates.

## How Conditionals Are Used

Conditional statements allow SpendWise to make decisions based on the user's budget and spending.

The application checks several budgeting situations:

1. No budget has been entered.
2. The user has spent more than the budget.
3. The user has used 80% or more of the budget.
4. The user is still within a safe spending level.

For example:

```javascript
if (budget <= 0) {
    statusTitle.textContent = "Ready to get started";
} else if (totalSpent > budget) {
    statusTitle.textContent = "You are over budget";
} else if (totalSpent >= budget * 0.8) {
    statusTitle.textContent = "You are approaching your limit";
} else {
    statusTitle.textContent = "You are within budget";
}