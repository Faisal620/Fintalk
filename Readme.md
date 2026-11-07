# FinTalk - Multilingual Conversational Loan Advisor

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://fintalk.streamlit.app/)

## Overview

**FinTalk** is an intelligent, AI-powered loan advisory platform that provides personalized financial guidance in multiple languages. Built with Streamlit and powered by Google's Gemini AI, FinTalk helps users make informed decisions about loans, credit, and financial planning.

## ✨ Key Features

- 🤖 **AI-Powered Chat**: Intelligent loan advisory using Google's Gemini 2.0 Flash model
- 🗣️ **Voice Support**: Speech-to-text and text-to-speech capabilities
- 🌐 **Multilingual**: Support for 11+ Indian languages including Hindi, Bengali, Tamil, Telugu, and more
- 💳 **Personal FinCard**: Customizable financial profile for personalized advice
- 🔒 **Secure**: API keys and sensitive data protection
- 📱 **Responsive**: Mobile-friendly interface
- 🎯 **Specialized**: Focused on loan eligibility, applications, and financial literacy

## 🚀 Live Demo

Try FinTalk live at: [https://fintalk.streamlit.app/](https://fintalk.streamlit.app/)

> **Note**: The live demo may have some limitations. For full functionality, follow the local setup instructions below.

## 🛠️ Local Setup

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)
- Git

### Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Faisal620/FinTalk.git
   cd FinTalk
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   
   # On macOS/Linux:
   source venv/bin/activate
   
   # On Windows:
   venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**
   
   Create a `.env` file in the project root:
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` and add your API keys:
   ```env
   # Get from: https://aistudio.google.com/app/apikey
   GOOGLE_API_KEY=your_google_api_key_here
   
   # Get from: https://www.sarvam.ai/
   SARVAM_API_KEY=your_sarvam_api_key_here
   ```

5. **Run the Application**
   ```bash
   streamlit run home.py
   ```

6. **Open in Browser**
   
   The app will automatically open at `http://localhost:8501`

## 🔑 API Key Setup

### Google API Key (Required)
1. Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Create a new API key
4. Add it to your `.env` file

### Sarvam API Key (For Audio Features)
1. Visit [Sarvam AI](https://www.sarvam.ai/)
2. Sign up for an account
3. Get your API key from the dashboard
4. Add it to your `.env` file

> **Security Note**: Never commit your `.env` file to version control. Keep your API keys secure.

## 📱 Usage Guide

### Getting Started
1. **Setup API Keys**: Configure your API keys in the API Key page
2. **Create FinCard**: Fill out your financial profile in the sidebar
3. **Start Chatting**: Ask questions about loans, credit, and financial planning

### Chat Features
- **Text Chat**: Type your questions in English or any supported language
- **Voice Chat**: Use the microphone to speak your questions
- **File Upload**: Upload audio files for transcription

### Supported Languages
- 🇮🇳 Hindi (हिंदी)
- 🇺🇸 English
- 🇧🇩 Bengali (বাংলা)
- 🇮🇳 Tamil (தமிழ்)
- 🇮🇳 Telugu (తెలుగు)
- 🇮🇳 Marathi (मराठी)
- 🇮🇳 Kannada (ಕನ್ನಡ)
- 🇮🇳 Gujarati (ગુજરાતી)
- 🇮🇳 Malayalam (മലയാളം)
- 🇮🇳 Punjabi (ਪੰਜਾਬੀ)
- 🇵🇰 Urdu (اردو)

## 🏗️ Project Structure

```
FinTalk/
├── home.py                 # Main application entry point
├── pages/                  # Modular application components
│   ├── main.py            # Chat functionality
│   ├── api_utils.py       # API integrations
│   ├── audio_utils.py     # Audio processing
│   ├── model_utils.py     # AI model management
│   └── text_utils.py      # Text processing utilities
├── config.py              # Configuration settings
├── requirements.txt       # Python dependencies
├── .env.example          # Environment template
├── .gitignore            # Git ignore rules
├── finCard_data.json     # User financial data
└── README.md             # This file
```

## 🔧 Configuration

### Environment Variables
- `GOOGLE_API_KEY`: Google Gemini API key (required)
- `SARVAM_API_KEY`: Sarvam AI API key (for audio features)
- `DEBUG`: Enable debug mode (optional, default: false)

### Customization
- Edit `config.py` to modify default settings
- Adjust language mappings and speaker preferences
- Customize UI elements and messages

## 🐛 Troubleshooting

### Common Issues

**Audio Recording Not Working**
- Ensure microphone permissions are granted
- Check if `streamlit-mic-recorder` is installed
- Try uploading an audio file instead

**API Errors**
- Verify your API keys are correct
- Check your internet connection
- Ensure you have sufficient API quota

**Language Detection Issues**
- Speak clearly and avoid background noise
- Try typing instead of using voice input
- Ensure the language is supported

**FinCard Data Not Saving**
- Check file permissions in the project directory
- Ensure `finCard_data.json` is writable

### Getting Help
If you encounter issues:
1. Check the troubleshooting section above
2. Review the application logs
3. Open an issue on GitHub with error details

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. **Fork the Repository**
2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make Your Changes**
4. **Run Tests** (if applicable)
5. **Commit Your Changes**
   ```bash
   git commit -m "Add amazing feature"
   ```
6. **Push to Your Branch**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**

### Development Guidelines
- Follow Python PEP 8 style guidelines
- Add docstrings to functions and classes
- Keep functions small and focused
- Handle errors gracefully
- Update documentation for new features

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Google AI** for the Gemini API
- **Sarvam AI** for multilingual speech services
- **Streamlit** for the amazing web framework
- **Contributors** who help improve FinTalk

## 📞 Support
- **Email**: [Contact the maintainer](mobasshirfaisal@example.com)

## 🗺️ Roadmap

- [ ] Integration with real loan providers
- [ ] Advanced financial calculators
- [ ] Document upload and analysis
- [ ] Loan comparison features
- [ ] Credit score improvement tracking
- [ ] Financial goal setting and tracking


*Empowering financial decisions through AI-powered conversations*
