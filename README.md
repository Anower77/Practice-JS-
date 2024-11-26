# Savings Calculator

This is a simple savings calculator that takes in an array of payments and a living cost, calculates the total income after tax deductions for payments over a certain threshold, and returns the resulting savings. If the savings are less than the living cost, it advises the user to "earn more."

## Features
- Calculates total income from an array of payments.
- Deducts 20% tax from payments greater than or equal to 3000.
- Compares the total income to the living cost to calculate savings.
- Returns the amount of savings or advises to "earn more" if savings are insufficient.
- Handles input validation for correct data types.

## Function

### `saving(payment, livingCost)`
Calculates savings based on payments and living cost.

#### Parameters:
- `payment` (Array): An array of payments (numbers) made during the month.
- `livingCost` (Number): The living cost for the month.

#### Returns:
- If the savings are greater than or equal to 0: Returns the savings amount.
- If the savings are less than 0: Returns the string `"earn more"`.
- If the input is invalid (non-array payments or non-number living cost): Returns the string `"Invalid input"`.

## Example Usage

```javascript
console.log(saving([1000, 2000, 3000], 5400)); // Output: 0
console.log(saving([1000, 2000, 2500], 5000)); // Output: 500
console.log(saving([900, 2700, 3400], 10000)); // Output: "earn more"
console.log(saving(100, [900, 2700, 3400])); // Output: "Invalid input"
