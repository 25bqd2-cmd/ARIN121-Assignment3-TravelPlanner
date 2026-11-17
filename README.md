# ARIN121-Assignment3-TravelPlanner

This travel planner extends the final Assignment 2 prompt with an activity menu and a guided conversation for choosing between destinations.

## What it does

- **Plan an itinerary:** creates morning, afternoon and evening activities for each day. It can estimate a budget, suggest indoor weather alternatives, and revise a specific day while preserving the rest.
- **Compare destinations:** collects two or three places and the traveller's priorities, compares the trade-offs, asks about a remaining concern, and uses the reply to refine its recommendation. It finishes when the traveller chooses or accepts a destination.
- **Revise a trip:** changes the requested part of an existing plan and checks the remaining constraints.

## How to use it

Copy the complete `system-prompt.md` into Google AI Studio Playground's System Instructions. A general request such as “Help me with travel planning” displays the three-option menu. Reply with a number, activity name, or a clear request in your own words. A direct activity request starts immediately. You can stop or switch activities at any point; relevant trip details should carry forward.

## Testing

Two fresh Playground conversations were tested on November 17, 2026 using Gemini 3.5 Flash Lite, Minimal thinking, maximum output 65,536 tokens, Default media resolution, and Google Search grounding enabled. Settings stayed the same.

1. The general request displayed the menu. Selecting 2 started destination comparison. A concern about hills and long walks changed the tentative recommendation from Quebec City to Montreal. Accepting Montreal ended the comparison with a recap and an offer to plan the itinerary.
2. A direct comparison request established a three-day duration, museums and food, and public transit. Switching in ordinary language to a Montreal itinerary retained those details and produced a three-day plan without requiring another menu selection.

The new menu, comparison and switching behavior met the two test goals. Travel descriptions and transport suggestions still need checking before a real trip; the assistant can sound more certain than the evidence warrants. Prices are estimates unless explicitly verified. Screenshots and observations are in the assignment submission document.

## Version history

The exact Assignment 2 prompt is preserved in the commit **Preserve Assignment 2 starting prompt** (`3e6d366`). The new prompt and this README were developed on `conversational-features` and reviewed through a pull request before merging into `main`.
