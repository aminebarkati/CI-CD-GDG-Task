# AI Agent Instructions for CI-CD-GDG-Project

This document guides AI coding agents on the key patterns and practices of this React-based chat application.

## Project Architecture

### Core Components
- Single-page React application with local storage-based chat functionality
- User context for managing authentication state
- Component-based architecture with clear separation of concerns

### Key Files and Their Roles
- `src/App.js`: Main application structure using React context for user management
- `src/local/chatStore.js`: Chat message management using localStorage
- `src/components/`: React components organized by feature
  - `ChatBox.js`: Main chat interface with message display and sending
  - `Message.js`: Individual message rendering
  - `NavBar.js`: Navigation and user interface
  - `Welcome.js`: Initial landing component

## Development Workflows

### Local Development
```bash
npm install  # Install dependencies
npm start    # Start development server
npm test     # Run tests
npm run build # Create production build
```

### State Management
- User state managed through React Context (`src/context/UserContext.js`)
- Chat messages stored in localStorage with `chatStore.js` utilities
- Message updates propagate through custom events (`chat-messages-updated`)

### Data Flow Patterns
1. Messages are stored locally using `chatStore.js` with:
   - `getMessages()`: Retrieves sorted messages (latest 100)
   - `addMessage()`: Adds new messages with unique IDs
   - `subscribe()`: Sets up real-time message updates
2. Components use the `useEffect` hook to subscribe to message updates

## Project-Specific Conventions

### Firebase Integration (Currently Disabled)
- Firebase configuration is prepared but commented out in `firebase.js`
- Environment variables expected to be prefixed with `REACT_APP_FIREBASE_*`

### Message Storage
- Messages are stored in localStorage under key `chat_messages_v1`
- Message format:
  ```javascript
  {
    id: string,
    text: string,
    name: string,
    avatar: string,
    uid: string,
    createdAt: number
  }
  ```

### Component Patterns
- Functional components with hooks
- Props destructuring for clear dependencies
- useRef for scroll management in chat
- useEffect for subscription cleanup

## Testing
- Jest and React Testing Library configured
- Tests expected to be co-located with components
- Run tests with `npm test`

## Build and Deployment
- Create React App standard build process
- Production builds created in `build/` directory
- Static assets optimized during build

For any changes or improvements to this documentation, please update this file while maintaining its structure and focus on project-specific patterns.