# ANN
\documentclass{article}
\usepackage{hyperref}
\usepackage{geometry}
\geometry{margin=1in}

\title{Neural Network Model for Income Prediction}
\author{}
\date{}

\begin{document}

\maketitle

\section*{Project Overview}

This repository contains the Python implementation and report for our group project, which developed a neural network model to predict individuals' likelihood of earning above \$50,000 based on demographic and socioeconomic data. The analysis and results are based on data from the U.S. Census Bureau.

\subsection*{Key Features}
\begin{itemize}
    \item \textbf{Prediction Goal}: Classify whether an individual's income is $\leq \$50,000$ or $> \$50,000$.
    \item \textbf{Performance}: Final model accuracy of \textbf{84.944\%} after hyperparameter optimization.
    \item \textbf{Significant Predictors}: Key factors influencing income predictions include:
    \begin{itemize}
        \item Capital gain
        \item Relationship status
        \item Educational attainment
        \item Occupational field
    \end{itemize}
\end{itemize}

\section*{Repository Structure}

\begin{verbatim}
├── Neural_Network_group_18_complete_code.ipynb   # Jupyter Notebook with the complete ANN code
├── 8413_Group_Assignment_3_Group18.pdf           # Detailed project report with analysis and insights
└── README.md                                     # Project description and documentation (this file)
\end{verbatim}

\section*{Data Preprocessing}

Before training the model, the dataset was processed to ensure data quality and compatibility with the neural network:
\begin{enumerate}
    \item \textbf{Missing Values}: Imputed missing values for categorical variables with the mode.
    \item \textbf{Feature Scaling}: Applied Min-Max scaling to normalize continuous variables.
    \item \textbf{Dummy Variables}: Converted categorical features into dummy variables to facilitate neural network processing.
    \item \textbf{Feature Alignment}: Ensured test and training datasets had identical feature sets by adding missing columns with zero values.
\end{enumerate}

\section*{Neural Network Configuration}

The final ANN architecture was optimized through cross-validation, yielding the following configuration:
\begin{itemize}
    \item \textbf{Input Layer}: 96 features
    \item \textbf{Hidden Layer}: 32 neurons with Sigmoid activation
    \item \textbf{Output Layer}: Binary classification using a Sigmoid function
    \item \textbf{Optimizer}: Stochastic Gradient Descent (SGD)
    \item \textbf{Learning Rate}: 0.01
    \item \textbf{Epochs}: 40
    \item \textbf{Batch Size}: 100
\end{itemize}

\section*{Results and Insights}

\begin{itemize}
    \item \textbf{Model Accuracy}: 84.944\%
    \item \textbf{False Negative Rate}: 10.66\% (tends to underpredict higher incomes)
    \item \textbf{False Positive Rate}: 4.86\%
    \item \textbf{Key Insights}:
    \begin{itemize}
        \item Higher education (e.g., Bachelor’s, Master’s) and professional roles correlate strongly with higher income.
        \item Married individuals and those with significant capital gains are more likely to earn above \$50,000.
    \end{itemize}
\end{itemize}

\section*{Usage}

\begin{enumerate}
    \item Clone the repository:
    \begin{verbatim}
    git clone https://github.com/your-username/your-repository.git
    \end{verbatim}
    \item Open the Jupyter Notebook file \texttt{Neural\_Network\_group\_18\_complete\_code.ipynb} to view or run the ANN model.
\end{enumerate}

\section*{Limitations and Future Improvements}

\begin{itemize}
    \item The model exhibits a class imbalance, leading to a higher false negative rate.
    \item Future iterations could implement techniques like SMOTE for class balancing or ensemble models to further improve accuracy and fairness.
\end{itemize}

\section*{Authors}

This project was completed by \textbf{Guiping Zhao}.

\end{document}

