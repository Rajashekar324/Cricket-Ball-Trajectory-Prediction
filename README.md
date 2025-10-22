![Screenshot 2025-04-30 131607](https://github.com/user-attachments/assets/64c4f874-4d70-43eb-8685-bb785f81b225)
*Problem Statement:*

In cricket, accurately tracking and predicting the trajectory of the ball is crucial for performance analysis, umpiring, and training. Traditional tracking systems like Hawk-Eye are expensive and require complex setups. The challenge was to develop a cost-effective computer vision–based system capable of detecting, tracking, and predicting the ball’s trajectory from standard video footage.

### *Proposed Solution:*

The project implements an *AI-powered computer vision pipeline* to detect and forecast the path of a cricket ball using video or image input.

1. *Data Collection & Augmentation:*

   * Collected image/video datasets of cricket ball deliveries.
   * Applied data augmentation (rotation, flipping, brightness adjustment) using Augmentation.py to increase dataset diversity.

2. *Ball Detection & Tracking:*

   * Used *OpenCV* to detect the ball in each frame using contour and color-based filtering.
   * Tracked the ball’s motion frame-by-frame to extract its positional coordinates (x, y).

3. *Trajectory Prediction Model:*

   * Trained a *machine learning regression model* (implemented in CricketTrajectory.ipynb) to predict the next coordinates of the ball based on previous positions.
   * Evaluated performance using Mean Squared Error (MSE) between predicted and actual trajectory points.

4. *Visualization:*

   * Predicted trajectories were visualized interactively through an HTML output (CricketTrajectory.html) showing the ball’s real and predicted path.

### *Tools & Technologies Used:*

* *Programming Language:* Python
* *Libraries:* OpenCV, NumPy, Pandas, scikit-learn, Matplotlib
* *Environment:* Jupyter Notebook
* *Supporting Files:* requirements.txt, run.bat for easy execution

