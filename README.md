# thesis_revival_project
# Driver Behavior Prediction: From Thesis to Autonomous Vehicle Systems

🚗 Project Overview

This repository represents a comprehensive revival and enhancement of my Master's thesis "Gap Acceptance Behavior in the Lane-Changing Model in Congested Traffic" (Southeast University, 2020). The original research analyzed driver heterogeneity in lane-changing decisions using the NGSIM US-101 dataset. This project rebuilds and extends that work with modern data science tools and machine learning techniques, specifically tailored for applications in Autonomous Vehicle (AV) behavior prediction.

🎯 Project Evolution
Phase	Status	Description
1. Thesis Replication	✅ Complete	Faithfully reproduced original thesis results using Python/Pandas instead of SPSS/Alteryx
2. Statistical Enhancement	🔄 In Progress	Fixed complete separation issues via regularization, improved model robustness
3. AV-Ready Features	📋 Planned	Added features relevant to AV systems (TTC, relative velocities, etc.)
4. Driver Clustering	📋 Planned	Unsupervised discovery of driver behavior classes using GMM
5. Production Simulation	📋 Planned	Integration with CARLA/SUMO simulators for AV testing

📊 Dataset

NGSIM US-101 Dataset (Federal Highway Administration)

    Location: Hollywood Freeway, Los Angeles, California

    Duration: 7:50 AM - 8:35 AM (June 15, 2005)

    Resolution: 10 Hz (0.1 second intervals)

    Vehicles Tracked: 6,101 vehicles

    Total Observations: ~4.5 million trajectory points

    Key Variables: Position (Global_X, Global_Y), Velocity, Acceleration, Lane_ID, Vehicle Class

Dataset available from: FHWA NGSIM Data Portal

🛠️ Technical Stack
Category	Tools
Programming	Python 3.9+
Data Manipulation	Pandas, NumPy
Visualization	Matplotlib, Seaborn, Plotly
Machine Learning	Scikit-learn, Statsmodels
Spatial Analysis	GeoPandas
Development	Jupyter Notebooks, VS Code, Git
Project Management	Todoist (task tracking)

 Repository Structure
 thesis_revival/
│
├── data/
│   ├── raw/                     (original NGSIM CSVs – untouched)
│   ├── processed/               (lane_change_events_classified.csv, etc.)
│   └── outputs/                 (tables, figures you already generated)
│
├── code/
│   ├── 01_data_exploration.ipynb
│   ├── 02_lane_change_identification.ipynb   (the clean version I provided)
│   ├── 03_modeling.ipynb                     (if you did Phase 3)
│   └── utils.py                               (reusable functions)
│
├── paper/
│   ├── draft_v1.docx (or .tex)
│   ├── figures/       (all graphs from your notebooks, exported as high‑res PNG/PDF)
│   ├── tables/        (CSVs of Table 8, comparison tables)
│   └── references.bib (or .ris)
│
└── notes/
│   ├── paper_outline.md
│   ├── writing_log.md      (daily progress)
│   └── to_do_list.md
├── .gitignore
├── requirements.txt
├── LICENSE
└── README.md                  # This file

🔬 Key Analyses
1. Lane Change Classification

    Mandatory Lane Changes (MLC): Merging (on-ramp) and Diverging (off-ramp)

    Discretionary Lane Changes (DLC): Overtaking, speed adjustment

    Method: Coordinate-based classification using GPS decision points from thesis

2. Driver Heterogeneity Analysis

    Original: Multinomial Logit Model with SPSS

    Improved: Regularized Logistic Regression with Scikit-learn

    Enhancement: Gaussian Mixture Models for unsupervised driver clustering

3. AV-Relevant Feature Engineering

    time_to_collision (TTC)

    relative_velocity_to_lead

    relative_velocity_to_lag

    time_headway

    gap_acceptance_probability


📈 Results & Validation
Thesis Replication Status
Thesis Component	Status	Accuracy
Table 8: Mean Values per Maneuver	✅ Complete	98% match
Graph 1a: Speed per Lane	✅ Complete	Visual match
Graph 1b: Speed per Section	✅ In Progress	-
Multinomial Logit Model	🔄 In Progress	-

Improvements Over Original Thesis

    Statistical Robustness: Fixed complete separation via L2 regularization

    Reproducibility: Full Python pipeline vs. proprietary SPSS/Alteryx

    Scalability: Handles full 4.5M rows efficiently

    Modern Features: AV-specific metrics added

    Version Control: Git tracking of all changes

🤝 Contributing

This is primarily a personal development project, but suggestions are welcome:

    Fork the repository

    Create a feature branch (git checkout -b feature/improvement)

    Commit changes (git commit -am 'Add some improvement')

    Push to branch (git push origin feature/improvement)

    Open a Pull Request

📚 Learning Journey

This project documents my transition from:

    Transportation Engineering → Data Science

    SPSS/Alteryx → Python/Pandas/Scikit-learn

    Academic Research → Industry Applications

Detailed learning notes available in docs/learning_log.md
🎓 Academic Reference

Original Thesis:
*Sangwa, N. (2020). Gap Acceptance Behavior in the Lane-Changing Model in Congested Traffic. Southeast University.*

Related Publication:
*Liu, Q., Sun, L., Kornhauser, A., Sun, J., & Sangwa, N. (2019). Road roughness acquisition and classification using improved restricted Boltzmann machine deep learning algorithm. Sensor Review, 39(6), 733-742.*

🔗 Connect

    LinkedIn: Nick Sangwa

    Email: nicksangwa@outlook.com

    Portfolio: Additional projects at GitHub Profile

📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
🙏 Acknowledgments

    Prof. Hu Wusheng (Southeast University) - Thesis supervision

    Federal Highway Administration - NGSIM dataset

    Open Source Community - Python data science ecosystem

    ChatGPT/DeepSeek - Technical guidance and code review

"Turning academic research into production-ready AV systems, one commit at a time."
