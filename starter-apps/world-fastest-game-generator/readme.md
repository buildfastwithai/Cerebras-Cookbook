# 🎮 World's Fastest Game Generator

⚡️ **Powered by Cerebras + Qwen-3 Series Models**

Generate complete HTML5 games in seconds using the power of Cerebras inference and Qwen-3 code generation models. This Streamlit app creates playable, standalone HTML games from simple text descriptions.

## ✨ Features

- **Lightning Fast**: Generate complete games in seconds using Cerebras' ultra-fast inference
- **Multiple Models**: Choose from Qwen-3 Coder models (480B, 235B variants)
- **Interactive Chat**: Iteratively improve your games through conversation
- **Standalone Games**: Creates complete HTML5 games that run in any browser
- **Download Ready**: Export your games as HTML files
- **Canvas-Based**: Generates modern HTML5 Canvas games with retry functionality

## 🚀 Quick Start

### Prerequisites

- Python 3.8+
- Cerebras API Key ([Get one here](https://cloud.cerebras.ai/))

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo/Cerebras-Cookbook.git
   cd Cerebras-Cookbook/starter-apps/world-fastest-game-generator
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the app**:
   ```bash
   streamlit run app.py
   ```

4. **Open your browser** and navigate to `http://localhost:8501`

## 🎯 How to Use

1. **Enter API Key**: Add your Cerebras API key in the sidebar
2. **Select Model**: Choose from available Qwen-3 models
3. **Describe Your Game**: Type a game idea like:
   - "Create a Snake game with neon colors"
   - "Make a space shooter with asteroids"
   - "Build a platformer with jumping mechanics"
4. **Generate**: Watch as your game is created in seconds
5. **Iterate**: Ask for improvements or modifications
6. **Download**: Save your game as an HTML file

## 🎮 Example Game Ideas

- **Classic Games**: Snake, Tetris, Pong, Pac-Man
- **Action Games**: Space shooters, platformers, endless runners
- **Puzzle Games**: Match-3, sliding puzzles, memory games
- **Arcade Games**: Breakout, Frogger, Centipede
- **Creative Games**: Drawing apps, music games, physics simulations

## 🧠 Available Models

| Model | Description | Best For |
|-------|-------------|----------|
| `qwen-3-coder-480b` | Largest code model | Complex games, advanced features |
| `qwen-3-235b-a22b-instruct-2507` | Instruction-tuned | Balanced performance |
| `qwen-3-235b-a22b-thinking-2507` | Reasoning-focused | Logic-heavy games |

## 🛠️ Technical Details

### Architecture
- **Frontend**: Streamlit for the web interface
- **AI Integration**: LangChain with OpenAI-compatible API
- **Inference**: Cerebras Cloud for ultra-fast model execution
- **Models**: Qwen-3 series for code generation

### Game Features
- HTML5 Canvas-based rendering
- Keyboard and mouse input handling
- Game loop with animation frames
- Collision detection
- Score tracking
- Retry/restart functionality
- Responsive design

### Code Structure
```
app.py              # Main Streamlit application
requirements.txt    # Python dependencies
readme.md          # This file
```

## 🔧 Configuration

### Environment Variables
You can also set your API key as an environment variable:
```bash
export CEREBRAS_API_KEY="your-api-key-here"
```

### Model Selection
The app supports multiple Qwen-3 models. Choose based on your needs:
- **480B**: Most capable, best for complex games
- **235B Instruct**: Good balance of speed and capability
- **235B Thinking**: Best for games requiring complex logic

## 📝 Example Prompts

### Game Creation
- "Create a Snake game with colorful graphics and smooth movement"
- "Make a space invaders clone with power-ups and multiple enemy types"
- "Build a simple platformer where the player collects coins and avoids enemies"

### Game Improvements
- "Add sound effects and background music"
- "Make the enemies move faster as the score increases"
- "Add a high score system that persists between games"
- "Change the color scheme to a dark theme"

## 🎨 Customization

The generated games include:
- **Visual Elements**: Colors, shapes, sprites, animations
- **Game Mechanics**: Physics, collision detection, scoring
- **User Interface**: Start screens, game over screens, controls
- **Responsive Design**: Works on desktop and mobile browsers

## 🚀 Performance

Thanks to Cerebras' Wafer-Scale Engine:
- **Generation Time**: 2-10 seconds for complete games
- **Model Size**: Up to 480B parameters
- **Throughput**: Extremely high tokens per second
- **Latency**: Sub-second response times

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is part of the Cerebras Cookbook and follows the same licensing terms.

## 🆘 Troubleshooting

### Common Issues

**API Key Error**
- Ensure your Cerebras API key is valid
- Check that you have sufficient credits

**Game Not Loading**
- Verify the generated HTML is complete
- Try regenerating with a simpler prompt

**Model Timeout**
- Switch to a smaller model if experiencing timeouts
- Simplify your game description

### Support

- **Documentation**: [Cerebras Cloud Docs](https://docs.cerebras.ai/)
- **API Reference**: [Cerebras API](https://cloud.cerebras.ai/)
- **Community**: [Cerebras Discord](https://discord.gg/cerebras)

## 🏆 Built With

- [Cerebras Cloud](https://cloud.cerebras.ai/) - Ultra-fast AI inference
- [Qwen-3 Models](https://qwenlm.github.io/) - Advanced code generation
- [Streamlit](https://streamlit.io/) - Web app framework
- [LangChain](https://langchain.com/) - AI application framework

---

**❤️ Built by Build Fast with AI**
