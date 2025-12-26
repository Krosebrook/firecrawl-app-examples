# AI Resume Job Matcher

An intelligent job matching system that automatically analyzes job postings against your resume using AI, with real-time notifications for matching positions.

## Features

- 🤖 AI-powered job matching using Claude 3 Sonnet
- 🔍 Automated job posting scraping
- 📄 Resume PDF parsing
- 💬 Discord notifications for matching jobs
- 🔄 Scheduled job checking
- 📊 Web interface for managing job sources
- 🗃️ Persistent storage with Supabase

## Use Cases

1. **Passive Job Seekers**: Automatically monitor multiple job boards and career sites without daily manual checking, receiving notifications only for roles that match your skills and experience.

2. **Career Transition Tracking**: Track job opportunities in new fields or industries while maintaining your current role, getting alerted when positions align with your transferable skills.

3. **Recruiter Portfolio Matching**: Recruiters can use this to match candidate resumes against multiple job postings simultaneously, identifying the best fits for their clients.

4. **Job Market Research**: Understand hiring trends and skill demands in your field by analyzing which types of positions match your profile over time.

## Prerequisites

- Python 3.10+
- [Supabase](https://supabase.com) account
- [Discord webhook](https://discord.com/developers/docs/resources/webhook) (for notifications)
- [Anthropic](https://www.anthropic.com) API key
- [Firecrawl](https://firecrawl.co) API key

## Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/ai-resume-matcher.git
   cd ai-resume-matcher
   ```

2. **Create a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**

   Create a `.env` file in the root directory with the following variables:

   ```bash
   FIRECRAWL_API_KEY=your_firecrawl_key
   ANTHROPIC_API_KEY=your_anthropic_key
   DISCORD_WEBHOOK_URL=your_discord_webhook_url
   RESUME_URL=your_resume_pdf_url
   SUPABASE_URL=your_supabase_url
   SUPABASE_KEY=your_supabase_key
   CHECK_INTERVAL_MINUTES=15
   ```

5. **Set up Supabase**

   Create a new Supabase project and create the following table:

   ```sql
   create table job_sources (
     url text primary key,
     last_checked timestamp with time zone
   );
   ```

## Running Locally

1. **Start the Streamlit web interface**

   ```bash
   streamlit run app.py
   ```

2. **Run the job checker scheduler**

   ```bash
   python -m src.scheduler
   ```

## Deployment

### GitHub Actions Scheduler

The project includes a GitHub Actions workflow that runs the job checker on a schedule. To set it up:

1. Add all environment variables from the `.env` file as GitHub repository secrets
2. The scheduler will run automatically every Monday (configurable in `.github/workflows/scheduler.yml`)

### Manual Deployment

1. Set up a server with Python 3.10+
2. Clone the repository and follow the local setup steps
3. Use a process manager like PM2 or Supervisor to run:

   ```bash
   # For the web interface
   streamlit run app.py

   # For the scheduler
   python -m src.scheduler
   ```

## Project Structure

- `app.py`: Main Streamlit web application
- `src/`
  - `scraper.py`: Job and resume parsing logic
  - `matcher.py`: AI-powered job matching
  - `discord.py`: Discord notification system
  - `database.py`: Supabase database operations
  - `models.py`: Pydantic data models
  - `scheduler.py`: Automated job checking

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
