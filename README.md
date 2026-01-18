# TremorScope

<div align="center">

![TremorScope Logo](https://img.shields.io/badge/🔬-TremorScope-06b6d4?style=for-the-badge)
![Version](https://img.shields.io/badge/version-2.0-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Demo](https://img.shields.io/badge/demo-live-brightgreen?style=flat-square)

**High-Precision Mouse Movement Analysis • Micro-Tremor Detection • AI Insights**

[Features](#-features) • [Quick Start](#-quick-start) • [Tracking Modes](#-tracking-modes) • [Metrics](#-metrics-explained)

</div>

---

## ✨ Features

### 🔬 Precision Tracking
- **60 FPS Sampling** — High-frequency movement capture
- **Sub-pixel Accuracy** — Detailed position tracking
- **Velocity & Acceleration** — Real-time speed analysis
- **Trail Visualization** — See your movement path

### 📈 Tremor Analysis
- **Micro-Tremor Detection** — Identifies involuntary movements
- **Jitter Measurement** — Quantifies movement irregularities
- **Direction Oscillation** — Detects back-and-forth patterns
- **Sliding Window Analysis** — Continuous pattern monitoring

### 🎮 Multiple Tracking Modes
- **Free Draw** — Open canvas for natural movement
- **Precision Test** — Structured movement challenges
- **Follow Target** — Chase the moving target for assessment

### 📊 Comprehensive Metrics
- **6 Primary Metrics** — Tremor, Jitter, Velocity, Acceleration, Direction, Hesitation
- **6 Advanced Metrics** — Smoothness, Curvature, Efficiency, Pauses, Avg/Peak Velocity
- **4 Real-time Charts** — Velocity, Tremor, Path, Direction distribution

### 🤖 AI-Powered Insights
- **Movement Assessment** — Behavioral pattern analysis
- **Verdict System** — Normal/Uncertain/Abnormal classification
- **Local Processing** — Privacy-first with Ollama
- **Contextual Feedback** — Practical insights

---

## 🚀 Quick Start

### Prerequisites
- Modern web browser (Chrome, Firefox, Edge)
- (Optional) [Ollama](https://ollama.ai/) for AI analysis

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/tremorscope.git
cd tremorscope

# Open in browser
start index.html  # Windows
open index.html   # macOS
xdg-open index.html  # Linux
```

### With Local Server
```bash
npx http-server . -p 8080
```

### Enable AI Analysis (Optional)
```bash
ollama run qwen2.5-coder:7b-instruct-q4_K_M
```

---

## 🎮 Tracking Modes

### Free Draw Mode
Open canvas for natural, unrestricted movement analysis. Best for general assessment.

### Precision Test Mode
Structured environment for controlled movements. Grid overlay helps visualize paths.

### Follow Target Mode
Chase a moving target around the canvas. Great for testing reaction time and precision under task pressure.

---

## 📊 Metrics Explained

### Primary Metrics

| Metric | Description | Good | Warning | High |
|--------|-------------|------|---------|------|
| **Tremor Index** | Involuntary movement measure | <0.5 | 0.5-1.5 | >1.5 |
| **Micro-Jitter** | High-frequency variations | <0.3 | 0.3-0.8 | >0.8 |
| **Velocity Var** | Speed consistency | <100 | 100-300 | >300 |
| **Acceleration** | Speed change rate | <500 | 500-1500 | >1500 |
| **Dir Changes** | Movement reversals | <20 | 20-50 | >50 |
| **Hesitations** | Pauses during movement | <5 | 5-15 | >15 |

### Advanced Metrics

| Metric | Description |
|--------|-------------|
| **Smoothness** | Movement fluidity (1.0 = perfect) |
| **Curvature** | Average path curvature |
| **Path Efficiency** | Direct vs actual distance (100% = optimal) |
| **Micro-Pauses** | Brief stops during movement |
| **Avg Velocity** | Mean movement speed (px/s) |
| **Peak Velocity** | Maximum recorded speed (px/s) |

### Friction Levels

- 🟢 **STABLE** — Normal, controlled movement
- 🟡 **MODERATE** — Some irregularity detected
- 🔴 **HIGH** — Significant tremor/friction present

---

## 🛠️ Technology Stack

| Component | Technology |
|-----------|------------|
| Tracking | Canvas API + requestAnimationFrame |
| Charts | [Chart.js](https://www.chartjs.org/) |
| Analysis | Custom tremor detection algorithms |
| AI | [Ollama](https://ollama.ai/) (local LLM) |
| UI | Vanilla JavaScript + CSS3 |

---

## ⚙️ Configuration

```javascript
// AI Settings
const OLLAMA_URL = 'http://localhost:11434';
const MODEL = 'qwen2.5-coder:7b-instruct-q4_K_M';

// Tracking Settings (in TremorScope class)
this.TREMOR_WINDOW_SIZE = 10;  // Samples for analysis
this.hesitationThreshold = 50;  // ms for hesitation
this.MAX_TRAIL = 300;  // Trail visualization length
```

---

## 🎯 Use Cases

- **Motor Control Research** — Study movement patterns
- **UX/UI Testing** — Analyze user interaction behavior
- **Accessibility Assessment** — Detect movement difficulties
- **Educational Demos** — Teach movement physics
- **Self-Assessment** — Personal movement tracking

---

## 🎨 UI Features

- **Cyan-Emerald Theme** — Scientific aesthetic
- **Real-time Charts** — Dynamic data visualization
- **Grid Overlay** — Precision reference
- **Gradient Trail** — Beautiful path visualization
- **Responsive Design** — Adapts to screen size

---

## 📄 License

MIT License — See [LICENSE](LICENSE) for details.

---

<div align="center">

**Made with ❤️ for the open-source community**

[Report Bug](../../issues) • [Request Feature](../../issues)

</div>
