Assignment Report
1. Setting Things Up
The notebook starts by hiding some unnecessary warnings.
It then loads the necessary tools:
PyTorch: For deep learning tasks.
Transformers library (Hugging Face): Provides pre-trained models for segmentation.
PIL, cv2, matplotlib, numpy: Libraries for handling and displaying images.
The notebook also checks if PyTorch is installed and confirms that it is running on the CPU (no GPU/CUDA available).

2. Object Segmentation
The main function in this notebook is segment_object. Here's what it does:
Loads an image (e.g., a picture of a chair) and converts it to RGB format.
Loads a pre-trained SegFormer model for segmenting objects in the image.
Processes the image to identify specific objects (like a "chair").
Creates a mask for the identified object (marks the part of the image where the chair is located).
Saves the segmented image (where the object is highlighted) and displays the mask.
In simple terms, this function scans the image, finds objects like a chair, and creates a mask that marks the object's location in the image.

3. Pose Editing
After identifying the object (e.g., a chair), the notebook uses another function to rotate the object and change its angle in the image.
This function, called edit_pose, uses the mask of the object (e.g., chair) to adjust its position in the image. In the example, the chair is rotated by 72 degrees.
The newly edited image is saved with a new filename (pose_edited_output.png).
4. Putting It All Together
The notebook demonstrates an example where:
An image of a chair is loaded.
The segmentation model is used to find and mask the chair in the image.
The chair's mask is displayed.
The chair is rotated (pose changed) and saved as a new image with the updated angle.
What Does It Do?
This notebook helps you:

Find objects in an image (e.g., a chair).
Create a mask for the object.
Edit the object (e.g., rotate it).
Outcome
By the end of the process, you will have:

A segmented image where the object is marked.
An edited version of the image where the object (e.g., the chair) is rotated.
