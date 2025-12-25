# AGI News ✨

AGI News is a daily AI newsletter that's completely sourced by autonomous AI agents.

This is an open-source project built with AI Agents, Resend, and Firecrawl 🔥

## Features

- Autonomous AI agents gather the latest AI news.
- Daily newsletter delivery.
- Frontend for subscribing to the newsletter.

## Use Cases

1. **Industry Newsletter Automation**: Automatically curate and distribute daily or weekly newsletters on any topic by deploying AI agents to gather relevant content.

2. **Competitive Intelligence Briefings**: Create automated briefings that track competitor announcements, product launches, and industry developments for business teams.

3. **Research Digest Generation**: Generate academic or technical digests by having agents monitor arxiv, research blogs, and publications in specific fields.

4. **Content Aggregation Service**: Build subscription-based content curation services where agents collect and synthesize information from multiple sources into themed newsletters.

## Installation

Clone the repository:

```bash
git clone https://github.com/ericciarla/aginews.git
```

### Frontend Setup

Navigate to the frontend directory:

```bash
cd /frontend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file with the following variables:

```env
SUPABASE_URL=
SUPABASE_SECRET_KEY=
RESEND_API_KEY=
```

Start the development server:

```bash
npm run dev
```

### Backend Setup

Navigate to the backend directory:

```bash
cd /backend
```

Install dependencies:

```bash
npm install
```

Create a `.env` file with the following variables:

```env
FIRECRAWL_API_KEY=
SUPABASE_URL=
SUPABASE_SECRET_KEY=
X_API_BEARER_TOKEN=
OPENAI_API_KEY=
RESEND_API_KEY=
```

Run the backend cron job:

```bash
ts-node src/index.ts
```

## Environment Variables

### Frontend

- `SUPABASE_URL`
- `SUPABASE_SECRET_KEY`

### Backend

- `FIRECRAWL_API_KEY`
- `SUPABASE_URL`
- `SUPABASE_SECRET_KEY`
- `X_API_BEARER_TOKEN`
- `OPENAI_API_KEY`
- `RESEND_API_KEY`

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.
