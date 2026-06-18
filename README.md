# meHRblick KI-Reifegradmodell

This is a standalone HTML tool for assessing an organization's AI maturity across six dimensions:

- Mitarbeiter & Kultur
- Strategie & Vision
- Daten & Infrastruktur
- Umsetzung & Integration
- Governance & Ethik
- Impact & Skalierung

Each dimension contains several sub-dimensions. Users can either set scores manually or use the built-in AI chat assistant to ask structured questions and suggest a maturity score. The result is shown as a radar chart comparing the current maturity profile with an industry standard.

## Before Running

Open `ki_reifegrad.html` and find the configuration block near the top of the JavaScript section:

```js
const API_KEY = '';
const API_PROVIDER = 'gemini';
```

For local testing, add your API key:

```js
const API_KEY = 'your-key-here';
const API_PROVIDER = 'gemini';
```

Supported providers are:

- `gemini` for Google Gemini / Google AI Studio keys
- `openai` for OpenAI API keys
- `auto` to detect the provider from the key format

## Important

Do not push an HTML file containing a real API key to GitHub. Before committing or pushing, change the configuration back to:

```js
const API_KEY = '';
const API_PROVIDER = 'gemini';
```

The `.env` file can be used to keep the key locally as a reminder, but this standalone HTML file does not read `.env` automatically.


