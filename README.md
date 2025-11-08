# ICT Assistant AI Chatbot - Red Team Evaluation Project

A comprehensive red team evaluation project for an ICT Assistant AI chatbot specialized in CSTA (Computer Supported Telecommunications Applications) standards using [promptfoo](https://promptfoo.dev/). This project tests the security, safety, and robustness of an AI assistant designed for ICT knowledge retrieval and chat.

## 📋 Project Summary

This project evaluates the "ICT AI Assistant Bot" - a RAG Chatbot that assists the user in CSTA related questions. The evaluation focuses on testing the chatbot's ability to:

- Stay within its defined scope (assist in developing applications and understanding the CSTA standards)
- Resist various attack vectors and prompt injection attempts
- Handle sensitive information appropriately
- Maintain appropriate responses across different scenarios
- Avoid harmful or inappropriate content generation

## 🎯 Key Features

- **Comprehensive Red Team Testing**: Multiple attack strategies including jailbreak, prompt injection, and adversarial techniques
- **Harmful Content Detection**: Evaluates responses to illegal activities, misinformation, privacy violations, and more
- **PII Protection**: Tests for direct personal information exposure vulnerabilities

## 🔧 Requirements

### System Requirements
- Node.js (v16 or higher)
- npm or yarn package manager
- Internet connection for API calls

### API Requirements
- Google AI/Gemini API key (`GEMINI_API_KEY` environment variable)

## 📦 Setup

1. **Install promptfoo globally**
   ```bash
   npm install -g promptfoo
   ```

2. **Set up environment variables**
   ```bash
   # Create a .env file or set environment variable
   export GEMINI_API_KEY="your-gemini-api-key-here"
   ```

3. **Verify installation**
   ```bash
   cd ict_assistant_red_team_evaluation
   promptfoo eval --var prompt="What is CSTA?"
   ```

## 🚀 Quick Start

1. **Run the red team evaluation**
   ```bash
   promptfoo redteam eval
   ```

2. **View results**
   ```bash
   promptfoo redteam report
   ```

## 📖 Usage

### Configuration Files

- **`promptfooconfig.yaml`**: Main configuration file containing:
  - Provider settings (Google Gemini 2.5 Flash)
  - Red team strategies and plugins
  - Test parameters and constraints
  - Output configuration

- **`redteam.yaml`**: Detailed red team configuration with:
  - Application purpose and domain information
  - User personas and data access definitions
  - Comprehensive plugin configurations
  - Attack strategies and parameters

### Running Evaluations

#### Basic Evaluation
```bash
promptfoo redteam eval
```

### Viewing Results

#### Web Interface
```bash
promptfoo redteam report
```

## 🛡️ Red Team Strategies

The evaluation includes multiple attack strategies:

1. **Jailbreak**: Single-shot optimization of safety bypass techniques
2. **GOAT (Generative Optimization of Adversarial Techniques)**: Dynamic multi-turn attack generation
3. **Prompt Injection**: Tests for direct prompt injection vulnerabilities

## 🔍 Test Categories

### Harmful Content
- Illegal activities handling
- Personal attacks and insults
- Misinformation and disinformation
- Privacy violation attempts
- Self-harm content
- Unauthorized professional advice
- Unsafe practices

### Security & Privacy
- PII (Personally Identifiable Information) exposure
- Competitor endorsement prevention
- Excessive agency detection
- Hallucination detection
- Hijacking prevention

## 🎛️ Configuration Options

### Environment Variables
- `GEMINI_API_KEY`: Required for Google Gemini API access

### Test Parameters
- `numTests`: Number of tests to run (default: 5)
- `maxConcurrency`: Maximum concurrent test executions (default: 1)
- `language`: Primary language for testing (Hungarian)

### Provider Settings
- Model: Google Gemini 2.5 Flash
- Delay: 100ms between requests. Only applies if `maxConcurrency` is set to 1
- API key configuration

## 🔧 Customization

### Adding New Test Cases
1. Modify `promptfooconfig.yaml` to adjust test parameters

### Modifying Attack Strategies
1. Update the `strategies` section in `promptfooconfig.yaml`
2. Adjust configuration parameters for each strategy
3. Add custom plugins as needed

If promptfooconfig.yaml changed, red team tests must be re-generated with running
```bash
promptfoo redteam generate
```

## 📈 Best Practices

1. **Regular Testing**: Run evaluations regularly during development
2. **Iterative Improvement**: Use results to refine the system prompt
3. **Monitor Trends**: Track evaluation results over time
4. **Document Findings**: Keep detailed records of vulnerabilities found
5. **Update Dependencies**: Keep promptfoo and plugins updated

## 🐛 Troubleshooting

### Common Issues

1. **API Key Errors**
   - Ensure `GEMINI_API_KEY` is set correctly
   - Verify the API key has proper permissions

2. **Installation Issues**
   - Check Node.js version compatibility
   - Try reinstalling promptfoo: `npm uninstall -g promptfoo && npm install -g promptfoo`

3. **Permission Errors**
   - Ensure write permissions for the output directory
   - Check file system permissions

### Getting Help

- Check the [promptfoo documentation](https://promptfoo.dev/docs)
- Review the generated error logs in the output directory
- Verify configuration file syntax

## 📝 License

This project is for educational and evaluation purposes. Please ensure you have proper permissions to use the Google Gemini API and any other services referenced.
