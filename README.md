# cf_ai_minxuan_jin
It is a AI chat robot contains LLM, Workflow, User input(chat), State supported by Cloudfare AI Platform.

## LLM part
Now use OpenAI GPT-4o-2024-11-20 model supported by OpenAI.

## Workflow
Uses Durable Objects and Workers for coordination:
- **Durable Object**: `Chat` class handles agent logic and state
- **Task Scheduling**: Supports one-time, delayed, and cron-based tasks
- **Tools**: Weather info, time lookup, task management

## User Input
Chat interface built with React:
- Real-time streaming responses
- Text input with auto-resize textarea
- Dark/Light theme toggle
- Human-in-the-loop tool confirmations

## Memory
Three-layer state management:
- **Durable Objects**: Persistent message history via `Chat` agent
- **Frontend**: React state with `useAgentChat` hook
- **LocalStorage**: User preferences (theme, etc.)

## Quick Start
```bash
cd chat
npm install
# Create .dev.vars with OPENAI_API_KEY=your_key
npm start
```