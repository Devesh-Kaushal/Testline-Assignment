# NEET Testline Performance Analysis & NEET Rank Prediction

This project analyzes student performance data from NEET Testline quizzes and generates actionable insights and recommendations. It also includes a bonus section that demonstrates a naive predictive model to estimate a student's NEET rank based on quiz performance metrics. This assignment is a test project to showcase your technical skills and approach. **Note:** The provided NEET dataset (`actual_neet_data.csv`) is a sample. For robust and production-grade predictions, please replace it with your actual dataset.

## Project Overview

The project is divided into several key components:

1. **Data Fetching & Loading:**  
   - **Current Quiz Data:** Fetched from a live API (data nested under the key "quiz").
   - **Quiz Submission Data:** Loaded from a local JSON file (`quiz_submission.json`).
   - **Historical Quiz Data:** Fetched from an API and normalized into a DataFrame with key fields (e.g., `accuracy_pct`, `quiz_title`).

2. **Data Processing & Analysis:**  
   - **Current Quiz Performance:** Accuracy is computed by comparing the student’s submitted answers against the correct answers.
   - **Historical Performance Analysis:**  
     - The historical DataFrame is processed to extract topics and convert accuracy values from strings to floats.
     - Topic-wise statistics are computed to identify weak topics (e.g., topics with average accuracy below 70%).
   - **Insights & Recommendations:**  
     - Insights are generated on overall performance, weak areas, and specific quiz metrics.
     - Recommendations are provided to guide targeted improvements.

3. **Bonus Analysis:**  
   - **Student Persona Analysis:**  
     The project assigns a creative label (e.g., "Consistent Achiever", "Struggling Learner", "Upward Trajectory Learner", or "Steady Performer") based on the comparison of historical and current quiz accuracies.
   - **Naive NEET Rank Prediction Model:**  
     A simple Random Forest-based model (or a placeholder naive model) predicts the student's NEET rank using features such as historical accuracy, current accuracy, total quizzes, and weak topic count.
     
     > **Important:** The current NEET rank prediction is based on a sample (simulated) dataset provided in `actual_neet_data.csv`. **For improved predictions, replace this file with your actual NEET dataset** that includes columns: `historical_accuracy`, `current_accuracy`, `total_quizzes`, `weak_topics_count`, and `neet_rank`.

4. **Visualizations:**  
   - Key visualizations (e.g., bar charts for average accuracy by topic) are generated using Matplotlib and Seaborn. Screenshots of these visuals are included in the `screenshots` folder.

5. **Demo Video:**  
   - A 2–5 minute demo video (`demo_video.mp4`) is provided to demonstrate the script/API, sample inputs/outputs, and a brief explanation of the logic and recommendations.

## Project Structure

```plaintext
.
├── README.md                   # This file: project overview, setup instructions, and approach description.
├── requirements.txt            # List of required Python packages.
├── instructions.txt            # Detailed instructions for setting up and running the project.
├── notebook.ipynb              # Jupyter Notebook containing all project cells.
├── neet_rank_predictor.joblib  # Saving the NEET rank prediction model.
├── quiz_submission.json        # Local JSON file containing quiz submission data.
├── actual_neet_data.csv        # Sample NEET dataset (replace with your actual data for robust predictions).
├── screenshots                 # Folder containing screenshots of key visualizations and insights.
└── demo_video.mp4              # A demo video (2–5 minutes) explaining the project.
