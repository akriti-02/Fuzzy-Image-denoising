# Fuzzy-Image-denoising
Denoising image using fuzzy membership functions and filters
Using Skfuzzy package from SciKit which is a tool box for SciPy.




# Noisy image
Add noise to the input images or ad noisy input image
![image](https://github.com/akriti-02/Fuzzy-Image-denoising/assets/142987817/bff30c0b-d930-4186-8c92-29a844fa5e10)

# Create various fuzzy filters for denoising the image 
 •	 Gaussian Fuzzy Filter with Median Centre [GMED]- It combines the concepts of Gaussian smoothing and median filtering with the use of fuzzy logic. 
![image](https://github.com/akriti-02/Fuzzy-Image-denoising/assets/142987817/26a67a32-736c-491f-809b-4f589cfce03c)

•	Sigmoidal Fuzzy Function:It is a fundamental concept of fuzzy logic. It models gradual transitions between membership values based on a sigmoid curve. 
![image](https://github.com/akriti-02/Fuzzy-Image-denoising/assets/142987817/17b6f10a-bcff-44f7-9852-d7b3dda3c133)

•	Gaussian Fuzzy Filter with Moving Average Centre [GMAV] - It combines Gaussian smoothening and moving average to reduce the noise from the image while preserving edges and details.
![image](https://github.com/akriti-02/Fuzzy-Image-denoising/assets/142987817/62878b02-0567-4d4f-ae3a-1ee9b3a9ba55)

Hybrid Fuzzy Filter:•	 In our code we combined the components:
	Mean Filter: Average the pixels within a local window [Square window] this smooths the images by reducing high- frequency noise.
	Median Filter: Replaces the central pixel values with the median value of the neighbouring pixels. This process is effective at removing impulse noise (salt & pepper).
	Fuzzy logic: We adapt filter behaviour based on local image characteristics i.e. we combine the results of mean and median filters using fuzzy rules.
	Hybrid approach: It combines the output mean and median filters. The weight factors (controlled by weight_mean) determines the balance between the two filters. The fuzzy logic component ensures adaptability to different noise patters.

![Untitled](https://github.com/akriti-02/Fuzzy-Image-denoising/assets/142987817/4c3d8eed-d910-480f-8d58-74ced3138b13)


We used PSNR to validate the performance
