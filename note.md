
<h2>Metric:</h2>
- **PSNR **<br>
- Peak Signalto-Noise Ratio*: metric to measure the similarity between the generated video frames and the ground truth frames <br>
- **SSIM(&#8593;) - Structure Similarity**: assesses the structural similarity between the generated and ground truth frames by considering luminance, contrast, and structural information <br>
- **MS-SSIM(&#8593;) - Multi-Scale Structure Similarity** <br>
- **CSIM(&#8593;) - Cosine Similarity**: evaluate identity preservation in the frames that have been generated. <br>
- **FID(&#8595;) - Frechet Inception Distance**: measures the distance between the feature representations of the generated and real video frames extracted from a pre-trained Inception network <br>
- **IS - Inception Score**: assesses the quality and diversity of the generated images by leveraging the output of a pre-trained Inception network. <br>
- **CPBD - Cumulative Probability Blur Detection**: assess image quality by detecting blur. <br>
- **LSE-D(&#8595;) - Lip Shape Evaluation - Distance Score**: evaluates the perceptual differences in lip shape between the generated frames and a reference method <br>
- **LSE-C(&#8593;) - Lip Shape Evaluation - Confidence Score/ Lip Sync Error - Confidence**: assesses the confidence in the generated lip shapes. It represents the confidence score associated with the lip shape generation. <br>
- **LMD(&#8595;) - Landmark Distance**:  evaluate whether the synthesized video corresponds to accurate lip movements based on the input audio <br>
- **LPIPS(&#8595;) - Learned Perceptual Image Patch Similarity** <br> 
- **Standard Deviation of Head Motion Feature Embeddings**: assesses the diversity of the generated head motions. extracted from the generated frames using Hopenet <br>
- **Beat Align Score**: used to evaluate the alignment between the audio and the generated head motions. represents a score that quantifies the synchronization of beats between the audio and the generated head motions. <br>
