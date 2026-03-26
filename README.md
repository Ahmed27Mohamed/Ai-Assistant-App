# 🤖 Snappy AI – Smart Egyptian AI Assistant

**Production-Level Android AI Chat Application built with Kotlin + MVVM + Firebase + Gemini AI**

🔗 **Live on Google Play**  
https://play.google.com/store/apps/details?id=com.chatai.snappy

---

## 📱 Overview

Snappy AI is a production-ready Android AI assistant application designed to provide a natural Egyptian Arabic conversational experience.

### The app integrates:

- 🔥 Google Gemini AI (gemini-2.5-flash-lite)
- 🗣 Speech-to-Text (Google Cloud STT)
- 🔊 Text-to-Speech (Speechify TTS)
- ☁ Firebase Authentication + Realtime Database
- 💾 Room Database (Offline Support)
- 🧠 Smart Persistent Memory System

Snappy AI behaves like a real Egyptian friend — conversational, contextual, personalized, and memory-aware.

---

# 📸 Screenshots

> Add your app screenshots inside a folder named `screenshots/` in your repository.

### 💬 Chat Interface
![Chat Screen](screenshots/chat.png)

### 🎤 Voice Input
![Voice Input](screenshots/voice.png)

### 🧠 Smart Memory Example
![Memory System](screenshots/memory.png)

### ⚙ Settings Screen
![Settings](screenshots/settings.png)

---

# 🚀 Key Features

## 🧠 1. Smart Memory System (Persistent AI Memory)

The assistant intelligently remembers:

- User name
- Governorate (Location)
- Area
- Interests
- Preferences

### How It Works

- Extracts structured data from user messages using a rule-based Memory Extractor.
- Stores memory under: users/{uid} in Firebase Realtime Database.
- Injects memory directly into Gemini `systemInstruction` for personalized responses.
- Supports long-term memory across conversations.

### Example

If a user says:

> "أنا من اسكندرية وبحب القهاوي"

The assistant:

- Saves Alexandria as governorate
- Saves cafés as interest
- Later recommends places accordingly

---

## 🗣 2. Voice AI (Full Duplex Experience)

### 🎤 Speech-to-Text
- Powered by Google Cloud Speech-to-Text
- Converts user voice into text in real time

### 🔊 Text-to-Speech
- Powered by Speechify TTS
- Automatically reads short AI responses
- Smart duration estimation
- Manual playback control

---

## 💬 3. Conversational AI (Gemini Integration)

- Uses Google Gemini 2.5 Flash Lite
- Custom Egyptian dialect system instruction
- Friendly, human-like tone
- Emotion-aware replies
- Context-aware conversation (last 10 messages)
- Memory injected via `systemInstruction` (not user prompt)

---


# 💎 Subscription System (Premium Plan)

Snappy AI includes a scalable subscription-ready architecture.

### 🔓 Free Plan
- Limited daily AI messages
- Basic memory support
- Standard response length
- Ads-ready architecture (optional)

### 💎 Premium Plan
- Unlimited AI conversations
- Extended memory capabilities
- Longer and more detailed AI responses
- Priority response generation
- Future advanced AI features
- Ad-free experience

### 🔧 Technical Implementation

- Stored under: users/{uid}/plan
- Plan types:
- `free`
- `premium`
- Ready for integration with:
- Vodafone Cash / Etisalat Cash / Orange Cash / We Pay
- Paymob
- Paypal

The architecture is already structured to support feature-gating based on subscription type.

---

## ☁ 4. Firebase Integration

### Firebase Authentication
- Google Sign-In
- User metadata stored:
  - uid
  - name
  - email
  - photoUrl
  - provider
  - subscription plan

### Realtime Database
Stores:
- Smart memory
- Chat messages
- Conversations

Includes automatic pruning to last 10 conversations.

---

## 💾 5. Offline Support (Room Database)

Stores:
- Conversations
- Messages
- Settings (AI name)

Features:
- Seamless fallback when offline
- Syncs when connection is restored

---

# 🏗 Architecture

- MVVM Architecture
- Repository Pattern
- Clean separation between:
  - AI Engine
  - Memory System
  - Firebase Layer
  - Local Database
- Coroutines + Dispatchers.IO
- State management via Compose `mutableState`

---

# 🧠 Smart Personalization Logic

### 🍽 Food Recommendations
- If governorate known → Suggest local places
- If unknown → Suggest famous Egyptian dishes
- Ask only one clarification question if needed

### 🌆 Outings
- Uses saved interests + location
- Adapts suggestions dynamically

---

# 🛠 Tech Stack

| Layer | Technology |
|--------|------------|
| Language | Kotlin |
| UI | Jetpack Compose |
| Architecture | MVVM |
| Local DB | Room |
| Cloud DB | Firebase Realtime Database |
| Authentication | Firebase Auth (Google Sign-In) |
| AI Model | Google Gemini 2.5 Flash Lite |
| TTS | Speechify |
| STT | Google Cloud Speech-to-Text |
| Networking | OkHttp |
| Concurrency | Kotlin Coroutines |

---

# 📂 Project Structure

ai/
└── GeminiAIEngine.kt

viewmodel/
└── ChatViewModel.kt

firebase/
└── FirebaseChatRepository.kt

database/
└── Room (DAOs + Entities)

tts_stt/
└── SpeechifyTTSManager.kt

memory/
└── UserMemoryRepository
└── MemoryExtractor


---

# 🔐 Security Note

⚠️ API keys should be moved to a secure backend or Cloud Function in production environments.

(Current implementation stores Gemini API key locally for development/demo purposes.)

---

# 🧪 Advanced Capabilities

- Long-term user memory
- Contextual conversation
- Egyptian dialect enforcement
- Voice-based interaction
- Offline-first architecture
- Conversation pruning system
- Smart AI system injection

---

# 📈 Production-Level Practices Applied

- Structured data persistence
- Cloud + Local hybrid storage
- Memory-based personalization
- Prompt engineering with system injection
- Separation of concerns
- Error handling with graceful fallback
- Network-aware sync logic

---

# 🎯 Why This Project Is Special

This is not just a chatbot.

It is:

- A contextual AI assistant
- With persistent identity memory
- Voice integration
- Offline resilience
- Cloud synchronization
- Real-world production architecture

---

# 👨‍💻 Developer

Ahmed Mohamed  
Android Developer | KMP | CMP

---

# 🏆 Status

✔ Production-Level  
✔ Cloud-Synced  
✔ Voice Enabled  
✔ Memory-Aware AI  
✔ CV-Ready Showcase Project
