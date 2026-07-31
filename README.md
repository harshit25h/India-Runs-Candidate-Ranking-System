# India.Runs Candidate Ranking System

An explainable candidate ranking system developed for the **India.Runs Data & AI Challenge** to rank **100,000 candidate profiles** against a target job description using skills, experience, behavioral signals, and other candidate attributes.

## 🎯 Problem Statement

Recruiters often need to identify suitable candidates from large talent pools. Simple keyword matching may fail to account for factors such as experience and candidate engagement.

The objective of this project is to:

- Evaluate candidate profiles against job requirements
- Rank candidates based on multiple relevant signals
- Generate a Top-N candidate shortlist
- Build a scalable and interpretable ranking pipeline

## 💡 Solution Approach

The system follows a multi-stage candidate ranking pipeline:

**Job Description → Candidate Processing → Feature Extraction → Signal Scoring → Weighted Ranking → Candidate Recommendations**

### 1. Candidate Profile Processing

The dataset contains **100,000 candidate profiles**. Candidate information is processed to evaluate relevant attributes such as:

- Technical skills
- Professional experience
- Recruiter response rate
- Interview completion rate
- Offer acceptance rate
- GitHub activity
- Profile completeness
- Open-to-work status
- Location

### 2. Feature Scoring

Each candidate is evaluated using four major scoring components.

| Component | Weight |
|---|---:|
| Skill Match | 40% |
| Experience | 25% |
| Behavioral Signals | 25% |
| Location | 10% |

### 3. Behavioral Signals

The behavioral component incorporates signals including:

- Recruiter response rate
- Interview completion rate
- Offer acceptance rate
- GitHub activity
- Profile completeness
- Open-to-work status

These signals complement technical skills and experience when ranking candidates.

### 4. Final Ranking

The component scores are combined into a weighted final score:

`Final Score = 0.40 × Skill Score + 0.25 × Experience Score + 0.25 × Behavioral Score + 0.10 × Location Score`

Candidates are then sorted by final score to generate the ranked shortlist.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Jupyter Notebook / Google Colab
- Git & GitHub

## 📁 Repository Structure

```text
India-Runs-Candidate-Ranking-System/
│
├── candidate_ranking.ipynb   # Candidate processing and ranking pipeline
├── sample_output.csv         # Example ranked candidate output
├── requirements.txt          # Python dependencies
├── .gitignore                # Files excluded from version control
└── README.md                 # Project documentation


```markdown
## 📊 Output

The system evaluates 100,000 candidate profiles and generates a ranked Top-100 shortlist based on skill alignment, experience, behavioral signals, and other relevant attributes.

The output contains:

- Candidate ID
- Rank
- Final score
- Recommendation reasoning

A small illustrative output is available in `sample_output.csv`.

## ▶️ How to Run

1. Clone this repository.
2. Install the required dependencies:

```bash
pip install -r requirements.txt
