# Tasks: Interactive Book with RAG Chatbot

**Input**: Design documents from `/specs/001-interactive-book-chatbot/`
**Prerequisites**: plan.md (required), spec.md (required for user stories), research.md, data-model.md, contracts/

## Phase 1: Setup (Shared Infrastructure)

- [X] T001 [P] Create `frontend` and `backend` directories.
- [X] T002 [P] Initialize `frontend` with Docusaurus.
- [X] T003 [P] Initialize `backend` with FastAPI.

---

## Phase 2: Foundational (Blocking Prerequisites)

- [ ] T004 [P] Set up Qdrant Cloud Free Tier and get credentials.
- [X] T005 [P] Implement text embeddings pipeline in `backend/rag/pipeline.py`.
- [X] T006 [P] Ingest initial book content into Qdrant.

---

## Phase 3: User Story 1 - Read and Navigate the Book (Priority: P1) 🎯 MVP

**Goal**: Users can read the book, navigate between chapters, and search for content.

**Independent Test**: The book is deployed on GitHub Pages and can be accessed through a URL. Users can click on chapter links to navigate, and use the search bar to find content.

### Implementation for User Story 1

- [X] T007 [P] [US1] Create initial book chapters (dummy content) in `frontend/docs/`.
- [X] T008 [P] [US1] Configure `docusaurus.config.js` and `sidebars.js` in `frontend/`.
- [ ] T009 [US1] Deploy the initial version of the book to GitHub Pages.

---

## Phase 4: User Story 2 - Ask General Questions to the Chatbot (Priority: P2)

**Goal**: Users can ask the chatbot questions about the entire book.

**Independent Test**: The chatbot widget is visible on the book's pages. Users can type a question and get an answer.

### Implementation for User Story 2

- [ ] T010 [P] [US2] Create React component `ChatbotWidget.jsx` in `frontend/src/components/`.
- [ ] T011 [P] [US2] Embed the `ChatbotWidget` in the Docusaurus layout.
- [ ] T012 [US2] Implement the `/chat` endpoint in `backend/main.py`.
- [ ] T013 [US2] Integrate OpenAI Agents/ChatKit in `backend/agents/handler.py`.
- [ ] T014 [US2] Connect the `ChatbotWidget` to the `/chat` endpoint.

---

## Phase 5: User Story 3 - Ask Questions About Selected Text (Priority: P3)

**Goal**: Users can select a piece of text and ask the chatbot a question about it.

**Independent Test**: Users can select text on a page, and a chatbot icon appears. Clicking the icon opens the chatbot with the selected text as context.

### Implementation for User Story 3

- [ ] T015 [P] [US3] Implement text selection capture in the frontend.
- [ ] T016 [US3] Send selected text context to the `/chat` endpoint.
- [ ] T017 [US3] Update the `/chat` endpoint to handle context.

---

## Phase N: Polish & Cross-Cutting Concerns

- [ ] T018 [P] Test chatbot for accuracy and relevance.
- [ ] T019 [P] Refine UI for better user experience.
- [ ] T020 [P] Final testing and debugging.
- [ ] T021 Deploy the full system (book + chatbot).

---

## Dependencies & Execution Order

- **Phase 1 & 2**: Can be done in parallel.
- **Phase 3**: Depends on Phase 1.
- **Phase 4**: Depends on Phase 2 and 3.
- **Phase 5**: Depends on Phase 4.

---

## Implementation Strategy

### MVP First (User Story 1 Only)

1. Complete Phase 1 & 2.
2. Complete Phase 3.
3. **STOP and VALIDATE**: Test User Story 1 independently.

### Incremental Delivery

1.  Complete Setup + Foundational → Foundation ready
2.  Add User Story 1 → Test independently → Deploy/Demo (MVP!)
3.  Add User Story 2 → Test independently → Deploy/Demo
4.  Add User Story 3 → Test independently → Deploy/Demo
