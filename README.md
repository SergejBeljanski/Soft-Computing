# Image and Video Processing

This repository contains my final-year assignments for the **Soft Computing** course, focused on picture and video processing. I explored various OpenCV functionalities, including Histogram of Oriented Gradients (HOG), Hough Transform, and custom color-based filtering techniques, to create this project. It uses OpenCV and NumPy to process videos and detect Buzzy Beetles (blue shells) crossing a vertical line within a defined region of interest.

## Key Highlights

### No Training Data
One of the core challenges I tackled was building this system **without any training data**. The detection and counting rely entirely on handcrafted color thresholds and algorithmic techniques, making it a pure rule-based approach.

### Concepts and Techniques Used
- **OpenCV HSV Filtering**: Used for isolating blue-colored objects based on HSV color space thresholds.
- **Contour Detection**: Identifies and tracks objects that match the specified criteria (size and position).
- **Bounding Boxes**: Visualizes detected objects on the frames for debugging and presentation.
- **MAE Calculation**: Computes the Mean Absolute Error (MAE) between predicted and expected object counts to assess performance.

## How It Works
The main functionality is divided into two parts:
1. **Video Processing**: Detects and counts blue objects (representing Buzzy Beetles) in each video frame as they cross a defined vertical line. The results are saved as output videos with visual overlays.
2. **Batch Processing**: Processes multiple videos using a metadata CSV file (`buzzy_beetle_count.csv`) containing video paths and expected object counts. It calculates the overall MAE for evaluation.


You can install the dependencies using the command:
```bash
pip install opencv-python numpy pandas
```

## Running the Code
To execute the project, use the Jupyter Notebook (`main_script.ipynb`). This is essential since the logic and execution steps are embedded in the notebook format.

1. Place your videos and the `buzzy_beetle_count.csv` file in the `data/` directory.
2. Open `main_script.ipynb` and run the cells sequentially.
3. The processed videos will be saved in the current directory with debug overlays showing detections and counts.

## Challenges and Learnings
- Developed a **rule-based detection** pipeline without the luxury of training data.
- Gained a deeper understanding of OpenCV features, particularly in color-based segmentation and contour analysis.
- Experimented with MAE as a metric to evaluate detection accuracy.
- Enhanced my problem-solving skills by debugging video processing workflows.

## Results
The project successfully identifies and counts Buzzy Beetles crossing a defined region in the videos with reasonable accuracy. The MAE metric provides insight into the system's performance and areas for improvement.

## Future Improvements
- Implement dynamic color thresholds to adapt to varying lighting conditions.
- Introduce machine learning to refine detection and reduce reliance on handcrafted parameters.
- Explore real-time video processing for live detection.

Feel free to reach out or contribute to this project! Thank you for checking out my work.

