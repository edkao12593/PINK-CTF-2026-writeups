# Sanity Check 2
**Category:** Misc  
**Tag:** Sanity / Discord  
**Points:** 50  
**Author:** QWERTZ

## Challenge

Did you really read the rules?!



## Solution

Unlike the first challenge, the second flag is not directly visible in the rules,still obvious but some can miss it,after all only less than half of the people get sanity check solve sanity check 2.

The challenge description suggests that we should examine the rules more carefully.

Looking at the Discord `#rules` message, we notice that the first character of each bullet point forms a hidden message. This technique is known as an **acrostic**.
<img width="1330" height="673" alt="image" src="https://github.com/user-attachments/assets/26aef72c-0212-4d5f-9743-6e3495fab470" />

Reading the first character of each rule from top to bottom gives:

`P · I · N · K · { · S · m · 4 · r · t · _ · B · 0 · y · ! · }`

Some rules have unusual beginnings, such as `4 People`, `_ is often used`, `0 day challenges`, and `! Please do not publish`. These are deliberately constructed to encode the flag.



Combining all the extracted characters produces the flag.

## Flag

`PINK{Sm4rt_B0y!}`
