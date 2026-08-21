# morning-board
Tom's personal morning board: ranch weather, local LLM buzz from X, AI shipped, browser tools

## Data sources
- **Weather**: Live from Open-Meteo API (Swift Ranch coordinates)
- **Local LLM on X**: `data/local-llm-x.json` (updated by external feed)
- **What shipped**: Hardcoded in HTML
- **Browser tools**: Client-side only (markdown, JSON, timezone)

## Updating Local LLM topics
Edit `data/local-llm-x.json` with fresh topics. See `data/README.md` for schema. The page auto-loads on refresh.
