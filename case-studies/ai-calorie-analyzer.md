# AI Meal & Calorie Analyzer

## Overview
A prototype AI system that analyzes food images and estimates calories and macronutrients.  
Designed for **anyone who wants quick nutritional insights** — from fitness enthusiasts and diet planners to general users, nutrition coaches, and doctors.

This tool demonstrates how AI can turn images into actionable information while keeping outputs structured and readable.

---

## Problem
People want instant calorie and nutrition estimates from food images.  
Existing solutions fail because:

- Portion sizes and angles are ambiguous  
- Mixed dishes are hard to parse  
- Local or uncommon foods often break the model  

The result: most apps either give **wrong numbers** or **hide uncertainty entirely**, leaving users guessing.

---

## Solution Architecture
The AI system is built as a simple, reliable workflow:

1. **Image input normalization** – ensures consistent image size and quality  
2. **AI food identification** – recognizes foods on the plate  
3. **Structured output generation** – calculates calories, protein, carbs, and fat  
4. **Confidence scoring** – flags uncertain predictions for clarity  

Even as a demo, the system provides users a **clear, easy-to-read breakdown** of their meals.

---

## What I Built
- A minimal UI for uploading food images  
- Backend AI based logic to process images and return structured nutrition data  
- Outputs that show calories and macronutrient breakdown per item  
- Clear formatting to help users immediately understand results  

**Example output (JSON)** after uploading a meal image:

```json
{
  "output": {
    "status": "success",
    "food": [
      {"name": "Grilled beef patty", "quantity": "150g", "calories": 330, "protein": 28, "carbs": 0, "fat": 25},
      {"name": "Cheddar cheese slice", "quantity": "30g", "calories": 120, "protein": 7, "carbs": 1, "fat": 10},
      {"name": "Lettuce leaf", "quantity": "15g", "calories": 2, "protein": 0.2, "carbs": 0.4, "fat": 0},
      {"name": "Tomato slices", "quantity": "30g", "calories": 5, "protein": 0.3, "carbs": 1, "fat": 0},
      {"name": "Burger bun (top and bottom)", "quantity": "100g", "calories": 270, "protein": 9, "carbs": 45, "fat": 4},
      {"name": "Mayonnaise sauce", "quantity": "20g", "calories": 140, "protein": 0, "carbs": 1, "fat": 15},
      {"name": "Potato fries", "quantity": "150g", "calories": 450, "protein": 5, "carbs": 60, "fat": 20}
    ],
    "total": {"calories": 1317, "protein": 49.5, "carbs": 107.4, "fat": 74}
  }
}
