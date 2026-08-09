---
name: asd-ste100
description: Write or rewrite technical prose in ASD-STE100 Simplified Technical English (Issue 9). Use when the user asks for STE, simplified technical English, plain technical language, or a controlled writing style for a guide, manual, or report. Applies short sentences, active voice, the command form, approved words, and consistent terms.
---

# ASD-STE100 writer

## Purpose

This skill writes and rewrites technical prose in ASD-STE100 Simplified Technical English (STE). STE is a controlled writing standard. It makes technical text easy to read. The standard is Issue 9 of ASD-STE100.

## When to use this skill

Use this skill when the user asks for one of these:

- STE or Simplified Technical English.
- A controlled or plain writing style.
- A rewrite of a manual, guide, or report.
- A rules check of existing prose.

Do not change this text when you use the skill:

- Code.
- Commands.
- JSON, XML, or YAML.
- Product names and proper nouns.
- Quoted text.
- Text on screens, labels, and placards.
- File paths and environment variables.

## Writing rules

Use all the rules in one text.

### Words and terms

- Use approved words with their approved meanings. (Rule 1.3)
- Use a technical noun or technical verb when it is the correct term. (Rules 1.5 and 1.12)
- Use a technical noun of 3 words or fewer. (Rule 2.1)
- Use the same term for the same item. (Rule 1.11)
- Use one meaning for one word. (Rule 9.2)
- Do not use slang, jargon, or regional words. (Rule 1.10)
- Use American English spelling. (Rule 1.14)

### Sentences

- Write 20 words or fewer in a procedure sentence. (Rule 5.1)
- Write 25 words or fewer in a descriptive sentence. (Rule 6.3)
- Write one instruction in each sentence. (Rule 5.2)
- Write a sentence with one topic only. (Rule 6.1)
- Write the condition first, then the command. (Rule 5.4)

### Verbs

- Write instructions in the command form. (Rule 5.3)
- Use the active voice. (Rule 3.6)
- Use the simple present, past, and future tenses only. (Rule 3.2)
- Do not use the `-ing` form, except in a technical noun. (Rule 3.5)
- Do not make phrasal verbs. (Rule 9.3)

### Punctuation

- Do not use a semicolon. (Rule 8.1)
- Use a hyphen to connect related words. (Rule 8.2)
- Use parentheses for a reference or an alternative. (Rule 8.3)
- Do not use Latin abbreviations such as `e.g.`, `i.e.`, or `etc.` (GR-6)

### Text structure

- Use a vertical list for a long series. (Rule 4.3)
- Write a note to give information only. (Rule 5.5)
- Use `WARNING` for risk of injury or death. (Rule 7.1)
- Use `CAUTION` for risk of damage to equipment or data. (Rule 7.1)
- Give the risk and the result in each safety instruction. (Rule 7.3)
- Keep the same wording for the same task. (Rule 9.4)
- Use the word `that` after `make sure`, `show`, and `recommend`. (GR-1)

### Word count

Count each of these items as one word (Rule 8):

- A number.
- A number with a unit of measure.
- An abbreviation.
- An alphanumeric identifier.
- Text in parentheses.
- A hyphenated group.
- Quoted text.
- A title or heading.

## Work flow

Do these steps in this order:

1. Read the full source text.
2. Find the technical nouns and verbs.
3. Keep each technical noun and verb as it is.
4. Replace each non-approved word with an approved word.
5. Split long sentences into short sentences.
6. Change the passive voice to the active voice.
7. Change each instruction to the command form.
8. Put the condition before the command.
9. Put a long series in a vertical list.
10. Remove every semicolon and contraction.
11. Use one term for each item in the whole text.
12. Count the words in each sentence.
13. Run the mechanical checks.

## Mechanical checks

Run these checks on the final text:

1. Search for semicolons in prose.
2. Search for contractions such as `don't` and `can't`.
3. Search for Latin abbreviations.
4. Search for passive voice verbs.
5. Search for phrasal verbs such as `set up` and `log in`.
6. Check the sentence length in each paragraph.

Useful commands:

```
rg -n ';' docs/
rg -n "don't|can't|won't|isn't|aren't|it's|doesn't" docs/
rg -n 'e\.g\.|i\.e\.|etc\.' docs/
rg -n '\b(is|are|was|were|has been|have been) +\w+(ed|en)\b' docs/
```

A contraction is two words written as one word with an apostrophe. Write the two words in full.

## Examples

### Example 1: split a long instruction

Before:

"To remove the cover assembly (9), first remove the four screws (10) that attach the cover (11) to the housing (12), and then, after taking the cover (11) off the housing (12), remove the preformed packing (13) and throw it away."

After:

1. Remove the four screws (10) that attach the cover (11) to the housing (12).
2. Remove the cover (11) from the housing (12).
3. Remove the preformed packing (13) and discard it.

### Example 2: change the passive voice

Before: "The temperature must be adjusted."

After: "Adjust the temperature."

### Example 3: do not omit words

Before: "If installed, remove the shims."

After: "If shims are installed, remove them."

### Example 4: use the word "that"

Before: "Make sure the valve is open."

After: "Make sure that the valve is open."

### Example 5: use a vertical list

Before: "The wheel assembly comprises the tire, the tube, the spokes, the spoke fittings, the valve, and the hub."

After:

"The wheel assembly has these parts:

- The tire
- The tube
- The spokes
- The spoke fittings
- The valve
- The hub."

### Example 6: write a safety instruction

"CAUTION: When you assemble the unit, do not let the parts fall. If they fall, damage to the parts can occur."

## Limits

This skill does not include the full STE dictionary. Use the rules in this skill and your knowledge of approved words. Keep company glossary terms when they exist. If a word is not approved, use a different sentence construction.

## References

See [references/RULES.md](references/RULES.md) for the full rule reference.
