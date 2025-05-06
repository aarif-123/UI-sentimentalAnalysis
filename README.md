# Multimodal Sentiment Analysis System
to run project write ##
npm run dev


A comprehensive system for analyzing sentiment in multimodal content, particularly videos, by combining visual, audio, and textual analysis.

## Features

- **Multimodal Analysis**: Combines visual, audio, and textual analysis for comprehensive sentiment understanding
- **Temporal Alignment**: Aligns different modalities to understand how they relate over time
- **Segment Analysis**: Breaks down videos into segments for detailed analysis
- **Modality Fusion**: Fuses results from different modalities using weighted averaging
- **Media Processing**: Utilities for extracting audio, frames, and segments from videos

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/multimodal-sentiment-analysis.git
cd multimodal-sentiment-analysis
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Usage

### Basic Usage

```python
from models.multimodal_analyzer import MultimodalAnalyzer

# Initialize the analyzer
analyzer = MultimodalAnalyzer()

# Analyze a video
results = analyzer.analyze_video('path/to/video.mp4', 'path/to/transcript.txt')

# Print the results
print(results['overall_sentiment'])
```

### Command Line Interface

The system also provides a command-line interface for easy usage:

```bash
python src/example.py --video path/to/video.mp4 --transcript path/to/transcript.txt --segment-duration 30 --output results.json
```

## Project Structure

```
.
├── src/
│   ├── models/
│   │   ├── __init__.py
│   │   ├── multimodal_analyzer.py
│   │   ├── visual_analyzer.py
│   │   ├── audio_analyzer.py
│   │   └── text_analyzer.py
│   ├── utils/
│   │   ├── __init__.py
│   │   └── media_utils.py
│   └── example.py
├── requirements.txt
└── README.md
```

## Dependencies

- Python 3.8+
- PyTorch
- Transformers
- MoviePy
- OpenCV
- NumPy
- SciPy

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- This project uses pre-trained models from Hugging Face Transformers
- Special thanks to the open-source community for their contributions
