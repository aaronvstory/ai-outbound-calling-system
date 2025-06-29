# AI-Powered Outbound Calling System

An automated customer support calling system powered by **Synthflow AI** that enables you to make intelligent outbound calls through a web interface.

## 🚀 Features

- **Web-based Interface**: Easy-to-use dashboard for creating and monitoring calls
- **AI-Powered Conversations**: Synthflow AI handles customer support interactions
- **Real-time Monitoring**: Live call status updates via WebSocket
- **Call Transcription**: Full conversation logs with success analysis
- **Error Handling**: Comprehensive error detection and user-friendly messages
- **Call Management**: Terminate calls, cleanup stuck sessions, view history

## 📋 Requirements

- Python 3.7+
- Synthflow AI account with API key
- Purchased phone number in Synthflow
- Flask and dependencies (see requirements.txt)

## 🛠️ Installation

1. **Clone the repository**:
   ```bash
   git clone <your-repo-url>
   cd Calls
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure your settings**:
   - Edit `config.py` with your Synthflow API key and phone number
   - Ensure your Synthflow assistant has a phone number assigned

4. **Run the application**:
   ```bash
   python app.py
   ```

5. **Access the web interface**:
   Open http://localhost:5000 in your browser

## ⚙️ Configuration

### Synthflow Setup
1. Sign up for [Synthflow AI](https://synthflow.ai)
2. Purchase a phone number
3. Create an assistant and assign the phone number
4. Generate an API key

### Application Setup
Update `config.py`:
```python
SYNTHFLOW_API_KEY = "your-api-key-here"
SYNTHFLOW_PHONE_NUMBER = "+1234567890"
DEFAULT_ASSISTANT_ID = "your-assistant-id"
```

## 🎯 Usage

1. **Create a Call**:
   - Enter your name and phone number
   - Specify the destination number
   - Describe the account action needed
   - Add any additional information

2. **Monitor Progress**:
   - Watch real-time status updates
   - View call transcripts when available
   - Terminate calls if needed

3. **Review History**:
   - See all past calls
   - Analyze success rates
   - Review conversation transcripts

## 🔧 Troubleshooting

### Common Issues

**Calls Stuck in Queue**:
- ✅ **FIXED**: The system now detects and prevents this issue
- Ensure your Synthflow assistant has a phone number assigned
- Run `python check_assistant.py` to verify configuration

**Connection Errors**:
- Verify your API key is correct
- Check internet connection
- Ensure Synthflow account is active

**Phone Number Issues**:
- Confirm phone number is purchased in Synthflow
- Verify number format (e.g., +1234567890)
- Check assistant configuration in Synthflow dashboard

## 📁 Project Structure

```
Calls/
├── app.py                      # Main Flask application
├── config.py                   # Configuration settings
├── requirements.txt            # Python dependencies
├── templates/
│   └── index.html             # Web interface
├── logs/                      # Application logs and database
├── check_assistant.py         # Diagnostic tool
├── fix_phone_issue.py         # Configuration fix script
└── ISSUE_RESOLUTION_REPORT.md # Detailed fix documentation
```

## 🔄 Recent Fixes

This version includes critical fixes for:
- ✅ Phone number configuration validation
- ✅ Enhanced error messaging
- ✅ Improved call status monitoring
- ✅ Better user interface feedback
- ✅ Comprehensive diagnostic tools

See `ISSUE_RESOLUTION_REPORT.md` for detailed information about resolved issues.

## 🚦 API Endpoints

- `POST /api/calls` - Create a new call
- `GET /api/calls` - Get all calls
- `GET /api/calls/<id>` - Get specific call details
- `POST /api/calls/<id>/terminate` - Terminate a call
- `POST /api/calls/cleanup` - Clean up stuck calls
- `GET /api/config` - Get system configuration
- `GET /api/phone-numbers` - Get available phone numbers

## 🔒 Security Notes

- Keep your API keys secure and never commit them to version control
- Use environment variables for sensitive configuration in production
- Consider implementing authentication for production deployments

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

[Add your license information here]

## 📞 Support

For issues related to:
- **Synthflow API**: Contact Synthflow support
- **This Application**: Create an issue in this repository
- **Configuration Help**: Run the diagnostic tools provided

---

**Note**: This system requires active Synthflow AI subscription and proper phone number configuration to function correctly.
