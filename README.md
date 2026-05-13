# JobCopilot AI

JobCopilot AI is an iPhone job-search companion built with SwiftUI and SwiftData. It helps users track applications on a visual Kanban board, organize profile data for different roles, and use AI to generate tailored job-search materials from a job description.

## What it does

- Tracks applications across Saved, Applied, Interview, Offer, and Rejected stages
- Supports multiple candidate profiles for different job targets
- Stores structured profile data such as experience, education, projects, skills, certifications, links, and AI memory notes
- Generates tailored resumes, cover letters, cold emails, recruiter replies, and interview prep
- Stores interview notes, reminders, and job-specific context in one place
- Shows pipeline and source breakdown stats
- Exports generated documents and job data

## Key features

### Visual job tracker
- Drag and drop jobs across a Kanban board
- Add jobs manually or paste a full job description for AI-assisted parsing
- Keep role, company, source, status, notes, and links together

### AI-powered application support
- Tailored resume generation
- Cover letter generation
- Cold email drafting
- Recruiter reply drafting
- Interview prep generation
- Rejection reflection
- Profile-grounded chat

### Interview and follow-up workflow
- Save interview questions, recruiter names, salary discussions, and tech stack details
- Add follow-up reminders
- Receive local reminder nudges and summaries

### Insights and exports
- Pipeline funnel and weekly activity views
- Source effectiveness breakdown
- Export jobs as CSV or PDF
- Share generated resumes and letters as PDF or RTF

## AI providers

The app currently supports user-supplied API keys for:

- Claude (Anthropic)
- OpenAI

Gemini and OpenRouter are scaffolded in the codebase but marked as coming soon in the UI.

## Privacy model

JobCopilot AI is built as a local-first app:

- No account or signup is required
- App data is stored locally with SwiftData
- AI provider API keys are stored in iOS Keychain
- AI requests go directly from the device to the provider the user selects
- No advertising SDKs or analytics SDKs are included in the app

## Tech stack

- Swift
- SwiftUI
- SwiftData
- URLSession
- UserNotifications
- BackgroundTasks
- Keychain Services

## Project structure

```text
JobCopilot AI/
├── JobCopilot AI/           # App source
│   ├── App/                 # App state and root flow
│   ├── Models/              # SwiftData models
│   ├── Services/            # AI, exports, notifications, persistence helpers
│   ├── Utilities/           # Shared constants and utilities
│   ├── ViewModels/          # Screen-level state and actions
│   └── Views/               # UI by feature area
├── JobCopilot AITests/      # Unit tests
└── JobCopilot AIUITests/    # UI tests
```

## Getting started

### Requirements

- Xcode
- A simulator or iPhone target
- An Anthropic or OpenAI API key if you want to test AI features

### Run locally

1. Clone the repository.
2. Open `JobCopilot AI.xcodeproj` in Xcode.
3. Select a signing team if Xcode asks for one.
4. Build and run the app.
5. Open Settings in the app and add an API key to enable AI features.

## Typical app flow

1. Create or select a profile.
2. Add a job manually or paste a job description.
3. Track that job on the board.
4. Generate tailored materials for the role.
5. Save notes, reminders, and outcomes as the process moves forward.

## Why this repo exists

This project explores what a focused, local-first AI productivity app can look like for job seekers: practical features, fast iteration, and direct utility without requiring a backend or account system.
