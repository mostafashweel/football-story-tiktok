# Football Story TikTok Generator 🎬⚽

Auto-generate and post faceless AI videos with football storytelling to TikTok - 10 videos per day!

## Features

✅ **Arabic Voiceover** - Generate stories in Arabic with text-to-speech  
✅ **English Subtitles** - Automatic translation and subtitle overlay  
✅ **Faceless Videos** - No camera/actors needed - just compelling storytelling  
✅ **Auto Posting** - Schedule 10 videos per day to TikTok  
✅ **Football Content** - Famous moments, player stories, match highlights  
✅ **Fully Automated** - Run once and it handles everything  

## Project Structure

```
football-story-tiktok/
├── config/
│   ├── config.py              # Configuration settings
│   └── .env.example           # Environment variables template
├── src/
│   ├── story_generator.py     # Generate Arabic football stories
│   ├── translator.py          # Translate to English
│   ├── audio_generator.py     # Arabic TTS voiceover
│   ├── video_creator.py       # Create video with subtitles
│   ├── tiktok_poster.py       # Post to TikTok API
│   └── scheduler.py           # Schedule 10 videos/day
├── assets/
│   ├── backgrounds/           # Background videos/images
│   ├── music/                 # Background music
│   └── fonts/                 # Font files for subtitles
├── logs/
│   └── app.log               # Application logs
├── main.py                   # Main entry point
├── requirements.txt          # Python dependencies
└── README.md                 # This file
```

## Installation

### Prerequisites
- Python 3.8+
- FFmpeg
- TikTok API credentials

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/mostafashweel/football-story-tiktok.git
cd football-story-tiktok
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Configure environment**
```bash
cp config/.env.example config/.env
# Edit config/.env with your API keys
```

## Configuration

Edit `config/.env` with:
- `OPENAI_API_KEY` - For story generation
- `GOOGLE_TRANSLATE_API_KEY` - For translation
- `GOOGLE_CLOUD_TTS_KEY` - For Arabic voiceover
- `TIKTOK_ACCESS_TOKEN` - TikTok API credentials
- `TIKTOK_BUSINESS_ACCOUNT_ID` - Your TikTok account

## Usage

### Run the generator
```bash
python main.py
```

### Generate a single video
```bash
python src/story_generator.py
```

### Test TikTok posting
```bash
python src/tiktok_poster.py --test
```

## How It Works

1. **Story Generation** → AI generates Arabic football story
2. **Translation** → Story translated to English
3. **Audio** → Arabic text-to-speech voiceover created
4. **Video** → Voiceover + background + English subtitles
5. **TikTok** → Post to your TikTok account
6. **Scheduler** → Repeat 10x per day automatically

## Story Topics

- ⚽ Famous football moments
- 👤 Player biographies
- 🎯 Match highlights
- 📊 Football facts & trivia
- 🏆 Tournament stories
- 🌟 Comeback stories

## API Integrations

- **OpenAI/Claude** - Story generation
- **Google Translate** - Arabic to English
- **Google Cloud TTS** - Arabic voiceover
- **TikTok API** - Video posting
- **FFmpeg** - Video processing

## Troubleshooting

### Audio not generating?
- Check Google Cloud TTS credentials
- Verify Arabic language support

### Subtitles not showing?
- Check font files in `assets/fonts/`
- Verify video codec compatibility

### TikTok posting fails?
- Verify access token not expired
- Check business account settings
- Review TikTok API rate limits

## Contributing

Feel free to submit issues and enhancement requests!

## License

MIT License

## Support

For issues and questions, open a GitHub issue.

---

**Made with ❤️ for football fans worldwide** ⚽🌍
