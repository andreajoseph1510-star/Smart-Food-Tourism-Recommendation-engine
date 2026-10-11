# Smart Food Tourism Recommendation Engine

An AI-powered food tourism recommendation workflow built with n8n that transforms travel preferences into personalized, data-driven itineraries.

## Problem Statement

Planning a trip often requires switching between multiple platforms to discover restaurants, explore tourist attractions, check weather conditions, and manage budgets. Combining all this information into a personalized day-by-day itinerary can be time-consuming.

## Solution

The Smart Food Tourism Recommendation Engine automates this process using data collection, feature engineering, recommendation scoring, budget planning, and generative AI to create a personalized travel itinerary.

## How It Works

1. **User Preferences:** Collects the destination, food preference, budget, trip duration, and travel style.
2. **Data Collection:** Retrieves restaurant and attraction information from OpenStreetMap through the Overpass API and weather information from Open-Meteo.
3. **Data Cleaning:** Extracts and standardizes relevant details, including cuisine, dietary options, location, and attraction categories.
4. **Recommendation Engine:** Ranks places using a scoring system based on food preferences, dietary compatibility, distance, attraction type, and weather conditions.
5. **Budget Planning:** Divides the available budget into planning allocations for meals and activities.
6. **AI Itinerary Generation:** Uses Google Gemini to turn the selected recommendations into a day-by-day itinerary.
7. **Database Integration:** Uses Supabase to store user travel preferences.
8. **Final Presentation:** Integrates Google Sheets with a Figma-inspired itinerary template to present the generated travel plan in a structured, visually appealing format.

## Tech Stack

- **Workflow Automation:** n8n
- **Generative AI:** Google Gemini
- **Database:** Supabase
- **Geospatial Data:** OpenStreetMap and Overpass API
- **Weather Data:** Open-Meteo
- **Output Integration:** Google Sheets and a Figma-inspired template
- **Data Processing and Scoring:** JavaScript

## Key Features

- Personalized food and travel recommendations
- Dietary preference-aware restaurant scoring
- Distance- and weather-aware ranking
- Budget allocation for meals and activities
- AI-generated daily itineraries
- Persistent storage of user preferences
- Structured, visually appealing itinerary presentation

## Project Workflow

User Preferences → Data Collection → Data Cleaning → Feature Engineering → Recommendation Scoring → Budget Planning → AI Itinerary Generation → Formatted Output

## Getting Started

### Prerequisites

- An n8n instance
- A Google Gemini API key
- A Supabase project
- Access to the OpenStreetMap Overpass API and Open-Meteo API
- Google Sheets configured for the final output integration

### Setup

1. Download the n8n workflow JSON from this repository.
2. Import the workflow into your n8n instance.
3. Configure the required credentials and integrations in n8n.
4. Set up the required Supabase database tables.
5. Configure the Google Sheets integration and connect your itinerary template.
6. Execute the workflow with your travel preferences.

**Security:** Configure credentials inside n8n. Never commit API keys, database secrets, passwords, or access tokens to GitHub.

## Limitations

- Restaurant prices and ratings may not be available in the source data.
- Recommendations depend on the coverage and accuracy of OpenStreetMap data.
- Budget allocations are planning estimates, not verified venue prices.
- Public API availability and
