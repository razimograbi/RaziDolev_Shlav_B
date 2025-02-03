# Global Communication Project

A near real-time voice communication system with AI-powered translation capabilities, enabling seamless cross-lingual conversations between users.


## Key Features
- Near real-time VoIP communication with low latency
- AI-powered speech-to-text (Whisper) and text-to-speech (XTTS/OpenAI TTS)
- Automatic language translation using ChatGPT 4o-mini
- Voice cloning support for supported languages
- Redis-powered audio chunk management
- Android client applications

## System Architecture
1. **Android Clients**: Capture/play audio and manage WebSocket connections
2. **FastAPI Server**: 
   - Handles WebSocket communication
   - Manages audio processing pipeline
   - Coordinates translation services
3. **Redis**: 
   - Stores audio metadata
   - Maintains chunk ordering
   - Manages conversation state
4. **AI Services**:
   - OpenAI Whisper (STT)
   - ChatGPT 4o-mini (Translation)
   - XTTS/OpenAI TTS (TTS with voice cloning)

## Installation

### Prerequisites
- Python 3.10+
- Android Studio (for frontend)
- Redis server
- OpenAI API key

### Clone Repository
```bash
git clone --recurse-submodules https://github.com/razimograbi/RaziDolev_Shlav_B.git
cd RaziDolev_Shlav_B

# If you forgot --recurse-submodules initially:
git submodule update --init --recursive
```
## Project Structure
├── backend@ # FastAPI server implementation
│ ├── main.py # Main server entry point and WebSocket handlers
│ ├── user.py # User management and authentication logic
│ ├── audioAccumulator.py # Audio chunk buffering and processing logic
│ └── externalAPIs.py # Integration with OpenAI, XTTS, and other external APIs
│
├── frontend@ # Android client application
│ ├── app/src/main/java/com/
│ │ ├── ActiveUser.java # Manages active user state and data
│ │ ├── ActiveUserAdapter.java # Adapter for active user list UI
│ │ ├── AudioRecordingActivity.java # Handles audio capture and playback
│ │ ├── AuthenticationService.java # Manages user authentication
│ │ ├── CallDashboardActivity.java # Main call interface and controls
│ │ ├── ErrorHandler.java # Centralized error handling
│ │ ├── FirestoreService.java # Firebase Firestore integration
│ │ ├── LoginActivity.java # User login screen
│ │ ├── MainActivity.java # Application entry point
│ │ ├── SignUpActivity.java # User registration screen
│ │ ├── User.java # User data model
│ │ └── WavRecord.java # Handles WAV audio recording logic
│
├── ShlavA/ # Phase A documentation and research materials
├── ShlavB_GloabCommunication # Final paper and technical documentation
├── Poster/ # Presentation poster materials
└── FinalVideoForGlobalCommunication # Demo video showcasing system functionality


# Contact
- Razi Mograbi - razi.mograbi@e.braude.ac.il
- Dolev Seri - Dolev.Seri@e.braude.ac.il
