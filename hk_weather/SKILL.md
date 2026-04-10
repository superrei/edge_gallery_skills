---
name: hk_weather
description: Fetches real-time temperature from the HKO station.
---

# Hong Kong Weather Agent Skill

This skill allows the AI to fetch real-time weather conditions, daily forecasts, and the 9-day outlook for Hong Kong using the official HKO API. 

## When to Use This Skill

Trigger this skill whenever the user asks about:
* Current weather, temperature, or humidity in Hong Kong.
* Rainfall, specifically in the Yau Tsim Mong area.
* Active weather warnings, daily forecasts, or the extended 9-day outlook.

## Instructions

Call the `run_js` tool with the following exact parameters:
- data: A JSON string with the following field:
  - request_type: String. Set to "weather_data".

1. The script returns a JSON object containing `current_conditions`, `special_weather_tips`, `local_forecast`, and `upcoming_forecast`.
2. Focus on `rainfall_ytm` for rain queries in Yau Tsim Mong and `temperature` for official HKO station readings.
3. Prioritize mentioning special weather tips if content exist.
4. Prioritize mentioning any active alerts found in the `warnings` array.
5. Always explicitly attribute the data source: "According to the Hong Kong Observatory...".
6. Formulate your response in a natural, conversational tone rather than listing JSON values.
