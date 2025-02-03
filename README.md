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
├── backend@ 
│   ├── main.py      
│   ├── user.py          
│   ├── audioAccumulator.py 
│   └── externalAPIs.py     
│
├── frontend@                 
│   ├── app/src/main/java/com/
│   │   ├── ActiveUser.java                    
│   │   ├── ActiveUserAdapter.java      
│   │   └── AudioRecordingActivity.java              
│   │   └── AuthenticationService,java               
│   │   └── CallDashboardActivity.java             
│   │   └── ErrorHandler.java              
│   │   └── FirestoreService.java
│   │   └── LoginActivity.java 
│   │   └── MainActivity.java  
│   │   └── SignUpActivity.java  
│   │   └── User.java  
│   │   └── WavRecord.java  
│
├── ShlavA/                 
├── ShlavB_GloabCommunication 
├── Poster/                 
└── FinalVideoForGlobalCommunication # Demo video of the system


# Contact
- Razi Mograbi - razi.mograbi@e.braude.ac.il
- Dolev Seri - Dolev.Seri@e.braude.ac.il
