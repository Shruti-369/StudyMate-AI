# FOLDER STRUCTURE

studymate-ai/
│
├── client/                        # React Frontend
│   ├── src/
│   │   ├── components/
│   │   │   ├── auth/              # Login, Signup forms
│   │   │   ├── quiz/              # Quiz UI, question cards
│   │   │   ├── chat/              # Doubt solver chat UI
│   │   │   ├── dashboard/         # Progress charts
│   │   │   ├── notes/             # PDF upload, RAG Q&A UI
│   │   │   └── common/            # Navbar, Loader, Button etc.
│   │   ├── pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── QuizPage.jsx
│   │   │   ├── ChatPage.jsx
│   │   │   └── NotesPage.jsx
│   │   ├── context/                # Auth context / Redux store
│   │   ├── services/                # api.js (axios instance)
│   │   ├── utils/
│   │   ├── App.jsx
│   │   └── main.jsx
│   └── package.json
│
├── server/                         # Node Backend
│   ├── config/
│   │   └── db.js                   # MongoDB connection
│   ├── models/
│   │   ├── User.js
│   │   ├── Quiz.js
│   │   ├── QuizResult.js
│   │   ├── ChatHistory.js
│   │   └── Notes.js                # stores chunks + embeddings
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── quizController.js
│   │   ├── chatController.js
│   │   ├── analyzerController.js   # weak-topic analysis
│   │   └── notesController.js      # RAG logic
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── quizRoutes.js
│   │   ├── chatRoutes.js
│   │   ├── analyzerRoutes.js
│   │   └── notesRoutes.js
│   ├── services/
│   │   ├── aiService.js             # Claude/OpenAI API calls centralized
│   │   ├── embeddingService.js      # embeddings generate + similarity search
│   │   └── pdfParser.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorMiddleware.js
│   ├── server.js
│   └── package.json
│
└── README.md                       # Design decisions, architecture, setup steps