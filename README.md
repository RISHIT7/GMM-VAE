# **GMM-VAE: Variational Autoencoder with Gaussian Mixture Model for MNIST Digit Classification**

### **Overview**  
This project explores the integration of a Variational Autoencoder (VAE) and a Gaussian Mixture Model (GMM) for classifying MNIST digits **1, 4, and 8**. The VAE encodes the input images into a continuous, low-dimensional latent space, and the GMM leverages this latent space to classify the digits.  

Key highlights of the project include visualizations of the latent space, reconstruction of the input images, and evaluation of GMM clustering performance.  

---

### **Features**  
- **2D Latent Space Representation**:  
  Visualizes how digits are encoded into a 2-dimensional Gaussian-distributed latent space, showing clustering and overlap.  

- **Image Reconstruction**:  
  Demonstrates the VAE's ability to reconstruct the MNIST digits from their latent representations.  

- **Latent Space Manifold Visualization**:  
  Provides insight into the smoothness and continuity of the learned latent space.  

- **GMM Clustering**:  
  Evaluates the clustering quality of digits in the latent space using Gaussian distributions.  

---

### **Project Structure**  

1. **Latent Space Visualization**:  
   - Highlights the 2D latent space for MNIST digits (1, 4, 8).  
   - Observes Gaussian distribution and identifies challenges in separation due to poorly written digits.  

2. **Reconstruction**:  
   - Recreates MNIST digits from the learned latent representations.  

3. **Latent Space Manifold**:  
   - Illustrates the smooth and continuous nature of the latent space.  

4. **GMM Clustering Visualization**:  
   - Visualizes Gaussian distributions (ellipses) for clustering.  
   - Assesses overlap and separation between clusters, highlighting areas for improvement.  

5. **Conclusion**:  
   - Successfully demonstrates VAE’s capability for representation learning.  
   - Suggests refinements to enhance cluster separation for improved classification accuracy.  

---

### **Usage**  

1. Clone the repository:  
   ```bash
   git clone https://github.com/RISHIT7/GMM-VAE.git
   cd GMM-VAE
   ```

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```

3. Train the VAE model and visualize results:  
   ```bash
   python train_vae.py
   ```

4. How to run the code
   ```bash
   # Running code for training. save the model in the same directory with name "vae.path"
   # Save the GMM parameters in the same folder. You can use pickle to save the parameters. 
   python vae.py path_to_train_dataset path_to_val_dataset train vae.pth gmm_params.pkl
  
   # Running code for vae reconstruction.
   # This should save the reconstruced images in numpy format. see below for more details.
   python vae.py path_to_test_dataset_recon test_reconstruction vae.pth
  
   #Running code for class prediction during testing
   python vae.py path_to_test_dataset test_classifier vae.pth gmm_params.pkl
   ```

---

### **Results**  

#### **Latent Space Visualization**  
Illustrates digit separation and clustering quality in the latent space.  

#### **Reconstruction**  
Reconstructed MNIST digits show the ability of the VAE to capture essential features.  

#### **Clustering with GMM**  
Evaluate overlap between Gaussian distributions and identify improvement areas for better classification.  

---

### **Authors**  
- **Rishit Jakharia**   
- **Aditya Jha** 

---

### **Acknowledgment**  
This work was completed as part of **COL333 Assignment 3.2** at **IIT Delhi** under the guidance of course instructors.
