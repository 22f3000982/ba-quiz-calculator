# Business Analytics Course Grade Calculator

A simple and intuitive web application built with React to help students in the Business Analytics course calculate their grades. This tool provides two main functionalities:
1.  **Quiz Passing Criteria Calculator**: Determines the minimum score needed in Quiz 2 to be eligible for the final exam.
2.  **Full Course Grade Calculator**: Calculates the final course score and letter grade based on all assessments.

## ✨ Features

-   **Dual Calculators**: Easily toggle between the Quiz Passing and Full Course Grade calculators.
-   **Dynamic Calculation**: Instantly see your results and eligibility status.
-   **Clear Eligibility Rules**: The tool checks and displays whether you meet the criteria for the final exam and final grade.
-   **Motivational Feedback**: Get congratulatory or encouraging messages based on your calculated grade.
-   **Responsive Design**: Accessible and easy to use on both desktop and mobile devices.

---

##  Grading Calculation Explained

The final course grade is determined by a combination of quizzes, assignments, and an end-term exam. Each component has its own weight and specific rules, which are detailed below.

### 1. Assessment Components

The total score is calculated out of **100 points**, broken down as follows:

-   **Quizzes (Qz)**: 20 points
-   **Assignments (A)**: 40 points
-   **End Term Exam (F)**: 40 points

### 2. Quizzes (Qz) - 20 points

There are two quizzes (Quiz 1 and Quiz 2), each marked out of 100. The scores are first scaled to be out of 20 (by dividing by 5).

The final quiz score (Qz) is a weighted average that gives more weight to your better performance.
The formula is:

**Qz = (0.7 × Max(Qz1_scaled, Qz2_scaled)) + (0.3 × Min(Qz1_scaled, Qz2_scaled))**

Where:
- Qz1_scaled = Quiz 1 score ÷ 5
- Qz2_scaled = Quiz 2 score ÷ 5

### 3. Assignments (A) - 40 points

There are three assignments, each marked out of 100. The scores are first scaled to be out of 20 (by dividing by 5).

The final assignment score (A) is the sum of your **best two** scaled assignment scores.
-   If you submit all three, the top two scores are added.
-   If you submit only two, their scores are added.
-   If you submit only one, only that score is considered.

The maximum possible score for this component is **capped at 40 points**.

### 4. End Term Exam (F) - 40 points

The End Term Exam is marked out of 100. The score is first scaled to be out of 45 using this formula:

**Scaled Score = Your Score (out of 100) × 0.45**

The final score for this component (F) is **capped at a maximum of 40 points**.

### 5. Eligibility Criteria 🛑

You must meet specific criteria to be eligible for the final exam and to receive a final course grade.

#### **Eligibility for the Final Exam:**

1.  Your final combined Quiz score (Qz) must be **at least 7 out of 20**.
2.  You must submit **at least one** of Assignment 1 or Assignment 2.

*If you do not meet both criteria, you are not eligible to sit for the End Term Exam.*

#### **Eligibility for a Final Course Grade:**

1.  You must be eligible for and attend the End Term Exam.
2.  Your final End Term Exam score (F) must be **at least 10 out of 40**.

*If you fail to meet these criteria, you will not receive a passing grade for the course, regardless of your total score.*

### 6. Final Score and Grade

If all eligibility criteria are met, your total score is calculated as:

**Total Score = Qz + A + F**

This total score (out of 100) is then mapped to a letter grade as follows:

| Total Score | Grade |
| :---------- | :---: |
| ≥ 89        |   **S** |
| ≥ 79        |   **A** |
| ≥ 69        |   **B** |
| ≥ 59        |   **C** |
| ≥ 49        |   **D** |
| ≥ 39        |   **E** |
| < 39        |   **F** |

---

## 💻 Technologies Used

-   **HTML5**
-   **CSS3**
-   **React.js** (via CDN)

---

## 👤 Author & Contact

This tool was created by **Ashish Raj**. Connect with me:

-   **Website**: [mauryahub.onrender.com](https://mauryahub.onrender.com/)
-   **LinkedIn**: [ashish-raj-02a700259](https://www.linkedin.com/in/ashish-raj-02a700259/)
-   **GitHub**: [22f3000982](https://github.com/22f3000982)
-   **Instagram**: [ashraj77777](https://www.instagram.com/ashraj77777)
-   **YouTube**: [@ashishmaurya7157](https://www.youtube.com/@ashishmaurya7157)