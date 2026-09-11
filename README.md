# Gita AI

Gita AI is a spiritual-conversation prototype that uses Groq-hosted language models to respond through Krishna, Ram, or Hanuman personas.

## Core features

- Landing page describing the spiritual chat experience.
- Chat interface with selectable Krishna, Ram, and Hanuman personas.
- Persona-specific system prompts and response styling.
- Multiple local chat threads with create, switch, and delete controls.
- Conversation history persisted in browser `localStorage`.
- Automatic retry handling for failed model requests.

## Technology stack

- Next.js 15 App Router and React 19
- JavaScript and Tailwind CSS 3
- Groq JavaScript SDK
- Framer Motion and next-themes

## Prerequisites

- Node.js compatible with the locked dependencies
- npm
- A Groq API key for chat responses

## Local setup

```bash
git clone https://github.com/varunisrani/gitaaii.git
cd gitaaii
npm ci
npm run dev
```

Production build and start commands:

```bash
npm run build
npm run start
```

Lint the project with `npm run lint`.

## Configuration

Create a local `.env` file and define only the variables you need:

- `GROQ_API_KEY` — required by the chat client
- `WEBSITE_URL` — optional site URL override
- `APP_NAME` — optional application-name override

Never commit API-key values.

## Project structure

- `app/page.js` — marketing landing page
- `app/chat/page.js` — persona selection, chat state, and Groq requests
- `app/components/` — shared theme control
- `config.js` — environment-backed runtime settings
- `next.config.js` — exported Next.js environment settings

## Status and limitations

This is an experimental client-side application, not an authoritative religious or counselling service. The current chat code sends requests directly from the browser and enables browser use in the Groq SDK, which exposes `GROQ_API_KEY` to clients; move model calls behind a server-side route before deployment. Several landing-page links are placeholders.
