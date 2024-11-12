# Mod10-check-algorithm

A Mod10 check algorithm is typically used to validate numerical data like credit card numbers, International Bank Account Numbers (IBAN), and other sequences where the integrity of the data needs to be checked. It relies on a checksum calculation to verify that the number is valid according to certain rules.

# Steps for Mod10 check

 - Start from the rightmost digit of the number (this is often called the "check digit").
 - Double every second digit from the right (i.e., the digits in odd positions when counting from the right starting with 1)
 - If doubling a digit results in a number greater than 9, subtract 9 from that number (or alternatively, you can sum the individual digits of the result, which is the same as subtracting 9 if the result is a two-digit number)
 - Sum all the digits, including the ones that were not doubled
 - Check the total sum: If the total sum is divisible by 10 (i.e., the sum modulo 10 is 0), then the number is valid according to the Mod10 check. If the sum is not divisible by 10, the number is invalid
