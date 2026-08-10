# Mike's Complete Roadmap: ML, Electronics & Business

**From 4th-year ECE student → ML/Electronics engineer + entrepreneur**

This is a personal, no-excuses, zero-wasted-time roadmap. Every item is
actionable. Follow the phases in order, but always keep the business lens on.

---

## The Big Picture

```
Phase 1 → Foundation & Tooling         (Weeks 1–4)
Phase 2 → ML/DS Core Mastery           (Weeks 5–16)
Phase 3 → Electronics from First Principles  (Weeks 9–20, parallel)
Phase 4 → Embedded ML / TinyML         (Weeks 17–28)
Phase 5 → Advanced AI + Signal Systems (Weeks 25–36)
Phase 6 → Build, Ship, Sell            (Ongoing from Day 1)
```

Run Phases 2 and 3 in parallel once you hit week 9. Business (Phase 6)
starts from Day 1 — not after you "feel ready."

---

## Phase 1 — Foundation & Tooling (Weeks 1–4)

### 1.1 Typing Speed

Bad typing bleeds hours every week. Fix it first.

| Goal | Tool | Daily time |
|------|------|-----------|
| Reach 60 WPM (touch-type) | [keybr.com](https://keybr.com) | 15 min/day |
| Reach 80+ WPM | [10fastfingers.com](https://10fastfingers.com) | 15 min/day |

**Rule:** Never look at the keyboard. Every session, every day, no exceptions.

### 1.2 Development Environment

Get this set up once and never fight tooling again:

```
1. VS Code  →  Python extension, Jupyter, Pylance, GitLens
2. Git      →  learn branching, commits, push/pull (you already use GitHub ✓)
3. conda or pyenv  →  virtual environments for every project
4. Linux basics   →  file system, bash commands, pipes
```

**Resources:**
- [Missing Semester of CS Education](https://missing.csail.mit.edu/) — covers shell, Git, editors in ~12 hours total
- [Pro Git Book](https://git-scm.com/book/en/v2) — free, chapters 1–3 are essential

### 1.3 Python Mastery

You know the basics. Now go deeper in 4 weeks:

| Topic | Resource | Hours |
|-------|----------|-------|
| OOP, decorators, generators | *Fluent Python* (ch. 1–7) | 10 h |
| NumPy — vectorization, broadcasting | Official NumPy quickstart + exercises | 6 h |
| Pandas — groupby, merge, reshaping | Kaggle Pandas micro-course | 4 h |
| Matplotlib / Seaborn | Practice on your existing notebooks | 4 h |
| Writing clean, readable code | PEP 8 + *Clean Code* excerpts | 3 h |

### 1.4 Math for ML — Quick Audit

You need these. If any column is weak, fix it in Phase 1:

| Topic | Why you need it | Self-test |
|-------|----------------|-----------|
| Linear algebra (vectors, matrices, eigenvalues) | Foundations of every ML model | Can you derive PCA by hand? |
| Calculus (chain rule, partial derivatives) | Backpropagation | Can you compute ∂L/∂w manually? |
| Probability & statistics (Bayes, distributions, hypothesis testing) | Model evaluation, data analysis | Can you explain p-value intuitively? |
| Optimization (gradient descent variants) | Training models | Can you code SGD from scratch? |

**Resources:**
- [3Blue1Brown — Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) (free, visual)
- [Khan Academy — Multivariable Calculus](https://www.khanacademy.org/math/multivariable-calculus) (free)
- *Mathematics for Machine Learning* — Deisenroth, Faisal, Ong ([free PDF](https://mml-book.github.io/))

---

## Phase 2 — ML/DS Core Mastery (Weeks 5–16)

You already have projects here (regression, classification). Now go wide and deep.

### 2.1 Supervised Learning (Weeks 5–8)

| Algorithm | What to do |
|-----------|------------|
| Linear & Logistic Regression | Implement from scratch with NumPy; understand the math |
| Decision Trees & Random Forests | Build one project (e.g., fraud detection) |
| Gradient Boosting (XGBoost, LightGBM) | Win Kaggle comps; use them on a tabular dataset |
| SVMs | Understand kernel trick; use sklearn |
| k-NN | Simple — implement it, understand bias-variance |

**Project idea:** Take a real ECE dataset (e.g., signal noise classification) and build an end-to-end pipeline.

### 2.2 Unsupervised Learning (Weeks 7–9)

| Algorithm | Project |
|-----------|---------|
| K-Means clustering | Customer/sensor segmentation |
| PCA | Dimensionality reduction on sensor time-series |
| DBSCAN | Anomaly detection in time-series signals |
| Autoencoders | Compress and reconstruct sensor data |

### 2.3 Model Evaluation & Engineering (Weeks 8–10)

This is where most beginners are weak. Master it:

- Confusion matrix, precision, recall, F1, ROC-AUC
- Cross-validation (k-fold, stratified)
- Hyperparameter tuning (GridSearch, Optuna)
- Feature importance and selection
- Handling imbalanced data (SMOTE, class weights)
- Data pipelines with `sklearn.Pipeline`

### 2.4 Data Science Workflow (Ongoing)

Every project must follow this:

```
1. Define the problem clearly (what decision does the model support?)
2. Collect / understand data
3. EDA → visualize distributions, correlations, outliers
4. Clean and preprocess
5. Baseline model (always start simple)
6. Iterate with better models / features
7. Evaluate rigorously (no data leakage!)
8. Document and share
```

### 2.5 Kaggle Practice

- Complete at least **2 Kaggle competitions** during Phase 2
- Read top kernels / notebooks after each competition
- Goal: land in top 30% on at least one competition

### 2.6 Recommended Courses

| Course | Platform | Cost |
|--------|----------|------|
| Machine Learning Specialization (Andrew Ng) | Coursera | Free audit |
| Practical Deep Learning for Coders | fast.ai | Free |
| Kaggle Learn — all tracks | Kaggle | Free |

---

## Phase 3 — Electronics from First Principles (Weeks 9–20)

Run **parallel** with Phase 2. Spend 1–2 hours/day on this track.

### 3.1 Circuit Theory Fundamentals (Weeks 9–11)

You've studied ECE for 4 years — now actually understand it:

| Topic | Resource | Hands-on |
|-------|----------|----------|
| Ohm's Law, KVL, KCL | *The Art of Electronics* ch. 1 | Breadboard RC, RL circuits |
| Op-amps | *The Art of Electronics* ch. 4 | Build a comparator, inverting amplifier |
| Filters (low-pass, high-pass, band-pass) | Same + YouTube | Measure frequency response with oscilloscope |
| Power supplies | Any practical guide | Build a regulated 5V PSU |

**Key Book:** *The Art of Electronics* — Horowitz & Hill. Read it cover to cover over Phase 3.

### 3.2 Digital Systems & Microcontrollers (Weeks 11–14)

| Platform | Why | Project |
|----------|-----|---------|
| Arduino Uno | Lowest barrier, huge community | Read sensors, control actuators |
| ESP32 | Wi-Fi + Bluetooth, cheap | IoT sensor node |
| Raspberry Pi | Linux SBC, runs Python | Bridge between hardware and ML |
| STM32 | Industry-grade ARM MCU | For later production-quality work |

**Learning path:**
1. Blink an LED → read a button
2. Read analog sensors (temp, light, sound)
3. UART / I2C / SPI communication
4. Send sensor data to a computer / cloud

### 3.3 Signal Processing (Weeks 13–17)

This is where ECE meets ML. Master this and you unlock a rare skill:

| Topic | Tool | Project |
|-------|------|---------|
| Fourier Transform / FFT | `numpy.fft`, SciPy | Frequency analysis of audio/vibration |
| Digital filters (FIR, IIR) | SciPy signal | Remove noise from sensor data |
| Spectrograms | Matplotlib, Librosa | Visualize audio/vibration as image |
| Sampling theorem (Nyquist) | Theory + simulation | Aliasing demo in Python |

```python
# Example: FFT on sensor data
import numpy as np
import matplotlib.pyplot as plt

# Simulate noisy 50Hz signal
fs = 1000  # sampling rate
t = np.linspace(0, 1, fs)
signal = np.sin(2 * np.pi * 50 * t) + 0.5 * np.random.randn(fs)

freqs = np.fft.rfftfreq(fs, 1/fs)
spectrum = np.abs(np.fft.rfft(signal))

plt.plot(freqs, spectrum)
plt.xlabel('Frequency (Hz)')
plt.ylabel('Amplitude')
plt.title('FFT of noisy 50Hz signal')
plt.show()
```

### 3.4 PCB Design (Weeks 17–20)

- Learn **KiCad** (free, industry-standard)
- Design your first PCB: microcontroller + sensor breakout
- Order from JLCPCB or PCBWay (~$5 for 5 boards)
- This is a portfolio piece and a sellable skill

---

## Phase 4 — Embedded ML / TinyML (Weeks 17–28)

This is the intersection of everything. Almost nobody in Ethiopia (or even
Africa) has this skill set deeply. This is your competitive moat.

### 4.1 What is TinyML?

Running machine learning models **on microcontrollers** with <1 MB of RAM.
Use cases:
- Keyword spotting ("Hey Siri") on a tiny chip
- Vibration anomaly detection on industrial machines
- Gesture recognition with an IMU (accelerometer/gyroscope)
- Predictive maintenance in factories

### 4.2 The TinyML Stack

```
Data collection (sensors) →
Python ML training (scikit-learn / TensorFlow) →
Model optimization (quantization, pruning) →
Deployment (TensorFlow Lite / Edge Impulse) →
Inference on MCU (Arduino, ESP32, STM32)
```

### 4.3 Learning Path

| Step | Resource |
|------|----------|
| 1. TensorFlow fundamentals | TensorFlow official tutorials |
| 2. TensorFlow Lite basics | TF Lite guide + examples |
| 3. TinyML book | *TinyML* — Warden & Situnayake (O'Reilly) |
| 4. Edge Impulse platform | [edgeimpulse.com](https://edgeimpulse.com) — free for makers |

### 4.4 TinyML Project Ideas (build all of these)

| Project | Hardware | Skill gained |
|---------|----------|-------------|
| Keyword spotting ("yes"/"no") | Arduino Nano 33 BLE Sense | Audio ML on MCU |
| Vibration anomaly detection | ESP32 + MPU6050 (accelerometer) | Industrial IoT |
| Gesture recognition | Raspberry Pi + camera | CV on edge |
| ECG anomaly detection | Wearable sensor + MCU | Biomedical ML |
| Predictive maintenance | Vibration sensor on motor | Production-ready project |

### 4.5 Deep Learning for Embedded Systems

| Topic | Why |
|-------|-----|
| CNNs | Image + spectrogram classification |
| RNNs / LSTMs | Time-series sensor data |
| Model quantization (INT8) | Fit models on MCUs |
| Knowledge distillation | Compress large models |
| Neural Architecture Search basics | Design efficient models |

---

## Phase 5 — Advanced AI + Signal Systems (Weeks 25–36)

### 5.1 Deep Learning (Systematic)

| Framework | Use case |
|-----------|----------|
| PyTorch | Research-grade flexibility, most used in academia |
| TensorFlow / Keras | Production deployment, mobile/embedded |

**Curriculum:**
1. Feedforward networks — understand backprop deeply
2. CNNs — image classification, object detection (YOLO)
3. RNNs, LSTMs, GRUs — sequence modeling
4. Transformers — attention mechanism, BERT, GPT basics
5. Transfer learning — fine-tune pretrained models on custom data

### 5.2 Advanced Signal Processing

- Wavelet transforms (better than FFT for non-stationary signals)
- Independent Component Analysis (ICA) — separating mixed signals
- Kalman filters — state estimation for dynamic systems
- OFDM and wireless signal processing (your ECE background becomes useful)

### 5.3 Computer Vision on Edge

- Object detection (YOLOv8) → quantize → deploy on Raspberry Pi
- Thermal camera + ML for industrial inspection
- Pose estimation for wearable applications

### 5.4 MLOps Basics

| Tool | Purpose |
|------|---------|
| MLflow | Experiment tracking |
| Docker | Containerize your models |
| FastAPI | Serve ML models as APIs |
| GitHub Actions | CI/CD for ML pipelines |

---

## Phase 6 — Build, Ship, Sell (Day 1 and Ongoing)

**Start this on Day 1.** Not after Phase 5. Not when you "feel ready." Now.

### 6.1 Portfolio Building

Every single project you build goes on GitHub with:
- Clear `README.md` (problem, approach, results, how to run)
- Jupyter notebooks with clean, documented code
- A demo GIF or screenshot

A strong GitHub profile IS your resume in this field.

### 6.2 Freelancing (Start at Month 3)

Where to get clients:
- **Upwork** — data science and ML projects
- **Fiverr** — "I will build your ML model / data analysis"
- **LinkedIn** — post insights, solutions to real problems; clients come to you
- **Local businesses / companies in Ethiopia** — massive untapped market

What to offer:
- Data analysis and dashboards (Power BI / Plotly Dash)
- Custom ML models for business problems (churn, demand forecasting)
- IoT sensor systems + data pipeline
- Embedded ML for local factories/industries

**Do this:** Solve one real problem for a local business for free or cheap
in Month 3. Get a testimonial. Use it as your first case study.

### 6.3 Product Ideas (Electronics + ML)

| Product | Market | Tech Stack |
|---------|--------|------------|
| Smart irrigation system | Ethiopian agriculture | Soil sensors + ESP32 + ML |
| Industrial vibration monitor | Local factories | Vibration sensor + TinyML |
| Low-cost ECG monitor | Healthcare | Bioamplifier + ML anomaly detection |
| Automated quality inspection | Manufacturing | Raspberry Pi camera + CNN |
| Grid fault detection | Power utilities | Current/voltage sensors + ML |

Each of these can become a product, a service, or a startup.

### 6.4 Business Mindset

**Frameworks to learn:**
- *The Lean Startup* — Eric Ries (build → measure → learn loop)
- *Zero to One* — Peter Thiel (thinking about creating new things)
- *$100 Startup* — Chris Guillebeau (start small, start now)

**Key principles:**
1. **Every skill you learn is a product** — ask "who would pay for this?"
2. **Ship before it's perfect** — a 70% done product with a user beats a
   perfect product that doesn't exist
3. **Solve real problems** — don't build solutions looking for a problem
4. **Document everything publicly** — blog posts, LinkedIn, GitHub = free marketing
5. **Network intentionally** — find 3 people in ML/electronics/business to follow
   and engage with every week

### 6.5 Income Milestones

| Milestone | How |
|-----------|-----|
| First $50 | Fiverr gig: data analysis / simple ML model |
| First $500 | Upwork contract: build an ML pipeline |
| First $2,000/month | Freelance retainer or 2–3 small clients |
| First product revenue | Launch one embedded ML product / dashboard tool |

---

## Do's and Don'ts

### DO

- ✅ Build one project per week during Phases 1–3, even if it's tiny
- ✅ Write about what you learn (LinkedIn post, GitHub README, anything)
- ✅ Break problems into 25-minute focused blocks (Pomodoro)
- ✅ Read for 30 minutes every day (technical or business)
- ✅ Push to GitHub every day you write code, no matter how small
- ✅ Join communities: fast.ai forums, Reddit r/MachineLearning, Edge Impulse Discord
- ✅ Track your study hours (use WakaTime — already in this repo)
- ✅ Review what you built each Sunday; fix one thing that's embarrassing
- ✅ Ask for help publicly — Stack Overflow, forums, GitHub Issues
- ✅ Set weekly goals every Monday morning (written down)

### DON'T

- ❌ Don't watch tutorial after tutorial without building anything (tutorial hell)
- ❌ Don't start a new course before finishing what's essential in the current one
- ❌ Don't wait until you "know enough" to start freelancing — start at Month 3
- ❌ Don't work on 5 things at once — one project at a time, done fully
- ❌ Don't ignore the business side until the end — it's part of the training
- ❌ Don't compare your Day 1 to someone else's Year 5
- ❌ Don't skip the math because it feels slow — it makes everything else faster
- ❌ Don't forget to sleep — seriously. 7 hours minimum. Fatigue destroys learning
- ❌ Don't build projects that nobody asked for — validate demand first
- ❌ Don't be shy about your work — share it, even if it's rough

---

## Weekly Schedule Template

| Time slot | Activity |
|-----------|----------|
| 06:00 – 06:15 | Typing practice (keybr.com) |
| 06:15 – 08:00 | Deep work: ML or Electronics study + coding |
| 08:00 – 09:00 | University / other obligations |
| 12:00 – 13:00 | Deep work: second session (math, projects) |
| 18:00 – 20:00 | Deep work: project building or reading |
| 20:00 – 20:30 | LinkedIn post, GitHub commit, review day |
| 21:00 – 22:00 | Business reading (*Lean Startup*, articles, etc.) |
| 22:00 | Sleep. 7 hours. Non-negotiable. |

Total: ~5–6 hours of focused work per day. More than enough to change your
trajectory in 12 months if done consistently.

---

## Milestones Checklist

### 30-Day Checkpoint
- [ ] Typing speed ≥ 60 WPM
- [ ] Dev environment fully set up
- [ ] Python OOP and advanced features reviewed
- [ ] NumPy and Pandas mastered beyond basics
- [ ] 1 new ML project pushed to GitHub

### 90-Day Checkpoint
- [ ] Completed 4+ ML projects (regression, classification, clustering)
- [ ] First Kaggle competition submitted
- [ ] Arduino: reading sensors and sending data to computer
- [ ] First freelance profile set up (Upwork or Fiverr)
- [ ] First blog post or LinkedIn article published

### 6-Month Checkpoint
- [ ] XGBoost / LightGBM models trained and evaluated on real data
- [ ] Signal processing with Python (FFT, filtering) solid
- [ ] ESP32 IoT node sending sensor data to a dashboard
- [ ] First paying freelance gig completed
- [ ] First TinyML model running on a microcontroller

### 12-Month Checkpoint
- [ ] Deep learning (CNN, RNN) projects in portfolio
- [ ] At least one embedded ML product prototyped
- [ ] PCB designed and ordered for a real project
- [ ] Consistent freelance income (>$500/month) or early-stage product
- [ ] Public GitHub profile with 10+ quality projects and daily activity

---

## Key Resources Summary

| Category | Resource | Free? |
|----------|----------|-------|
| Shell / Git / Dev tools | [Missing Semester](https://missing.csail.mit.edu/) | ✅ |
| ML fundamentals | [Andrew Ng ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction) | Free audit |
| Deep learning | [fast.ai](https://fast.ai) | ✅ |
| Practice | [Kaggle](https://kaggle.com) | ✅ |
| Math for ML | [mml-book.github.io](https://mml-book.github.io/) | ✅ |
| Electronics | *The Art of Electronics* — Horowitz & Hill | Book |
| TinyML | *TinyML* — Warden & Situnayake | Book |
| TinyML platform | [Edge Impulse](https://edgeimpulse.com) | ✅ maker |
| Linear algebra (visual) | [3Blue1Brown](https://www.3blue1brown.com/topics/linear-algebra) | ✅ |
| Business | *The Lean Startup* — Ries | Book |
| Business | *Zero to One* — Thiel | Book |

---

*Last updated: March 2026*
*This roadmap lives in the repo — update it as you progress.*
