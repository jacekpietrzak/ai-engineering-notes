# Prompt Engineering - Data Extraction

## 🎯 Objective
Creating effective prompts to extract specific data formats while maintaining accuracy and avoiding common pitfalls.

## 📝 Case Study
Source data: Text containing a token in XXXX-XXXX-XXXX format (where X represents digits) mixed with other content.

## 🔄 Process Evolution

### Initial Attempts
Various approaches were tested, each teaching valuable lessons about prompt construction:

1. **Basic Approach**
Instruction: Analyze the text and return ONLY the digit sequence in XXXX-XXXX-XXXX format.
Result: Insufficient - didn't handle edge cases

2. **Detailed Specification**
Analyze the text and return ONLY the digit sequence that meets ALL conditions:
- Contains exactly 4 digits, then hyphen
- Then exactly 4 digits, then hyphen
- Then exactly 4 digits
Result: Added unwanted explanatory text

## ✅ Working Solution
Find and return the existing digit sequence in the format:  
```four digits, hyphen, four digits, hyphen, four digits.```  
```Do not generate a new sequence. Return only the one that exists in the text.```  
```Return ONLY the digit sequence in XXXX-XXXX-XXXX format from the text. Without any additional text or explanations.```  

## 🔍 Key Learnings
1. Redundancy in prompts can improve accuracy
2. Explicit instructions about what NOT to do are important
3. Multiple format descriptions help ensure correct pattern matching
4. Final instruction should be very specific about output format

## 💡 Best Practices
1. **Clear Instructions**
   - Be explicit about searching vs. generating
   - Specify output format clearly
   - Include safeguards against common errors

2. **Effective Structure**
   - Use redundancy strategically
   - Combine different ways of describing the same requirement
   - End with specific output format instructions

3. **Error Prevention**
   - Explicitly state what not to do
   - Prevent common mistakes (like adding explanatory text)
   - Emphasize existing data extraction over generation

## 📚 Applications
This approach can be adapted for various data extraction tasks where precise format matching is required.
