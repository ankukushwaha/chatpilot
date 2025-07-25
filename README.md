# 🟢 Real-Time Chat Support Dashboard (React + Socket.IO)

This is a **real-time customer support chat application** built using **React.js**, **Socket.IO**, and **Bootstrap**. The application simulates a customer support dashboard where support agents can interact with multiple visitors, view their message history, and see real-time updates.

---

## 🚀 Features

### ✅ Functionalities Implemented

1. **Three-column layout**:
   - **Left Panel**: List of connected visitors.
   - **Middle Panel**: Chat window of selected visitor.
   - **Right Panel**: Visitor profile + last 5 chat history entries.

2. **Single Visitor Selection**:
   - Only one visitor can be selected at a time.
   - Selected visitor's messages are shown in the chat window.

3. **Unread Message Counter**:
   - When a visitor sends a new message and is not selected, a counter and highlight appear on their name.

4. **Real-time Messaging**:
   - Messages are sent and received in real-time using Socket.IO.
   - If selected visitor sends a message, it is immediately shown in the chat window.

5. **Message Highlighting**:
   - New visitor messages are briefly highlighted and fade out.
   - Highlight also fades if user responds.

6. **Aligned Messages**:
   - Visitor messages appear on the left.
   - Support/User messages appear on the right.

7. **Hover Actions**:
   - Hovering over any visitor message shows two icons:
     - 💬 **Chat Details**
     - 📄 **Chat Summary**

8. **Modals for Chat Details & Summary**:
   - Clicking icons opens a modal displaying:
     - Full detail of selected chat.
     - Summary including visitor + user messages.

9. **Persistent State with `localStorage`**:
   - Selected visitor, unread counts, and chat messages persist across refreshes.

---

## 🧱 Tech Stack

- **Frontend**: React.js, Bootstrap 5
- **Real-time Communication**: Socket.IO
- **State Management**: React Hooks
- **Storage**: LocalStorage

---

## 🗃️ Data Structures Used

| Structure              | Type                    | Purpose                                         |
|------------------------|-------------------------|-------------------------------------------------|
| `visitors`             | Array of Objects        | List of connected visitors                      |
| `selectedVisitorId`    | String                  | Tracks current selected visitor                 |
| `messages`             | Object (id → Array)     | Stores messages per visitor                     |
| `unreadCounts`         | Object (id → int)       | Tracks unread message count                     |
| `highlightedMessages`  | Set or Object           | Temporarily tracks messages to be highlighted   |
| `localStorage`         | Key-Value Store         | Stores persistent UI state across reloads       |

---

## 📁 Project Structure

client/
├── public/
├── src/
│ ├── components/
│ │ ├── VisitorList.jsx # Left panel: visitor list
│ │ ├── ChatWindow.jsx # Middle panel: selected visitor chat
│ │ ├── VisitorProfile.jsx # Right panel: visitor profile + history
│ │ ├── Modal.jsx # Modal for chat detail/summary
│ ├── App.jsx
│ ├── index.js
server/
├── SocketHandler.js # Socket.IO logic (emit, listen)
├── App.js # Express app
├── server.js # Server entry point



---

## ⚙️ Getting Started

### 🔧 Prerequisites

- Node.js and npm installed

### ▶️ Run Project Locally

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/ankukushwaha/chat-dashboard.git
   cd chat-dashboard


Install Dependencies

Backend:

cd Backend
npm install

Frontend:

cd chatpilot
npm install

start the Backend:
node server.js
Open http://localhost:5000 in the browser.

Start the React App:
npm run dev
Open http://localhost:5173 in the browser.

📄 License
This project is for learning/demo purposes. You may use, extend, or contribute freely.

🙌 Author
Ankur Kumari Kushwaha
React | Node.js | Full Stack Projects


---

Let me know if you want the markdown converted into a downloadable `.md` file or hosted on GitHub.






