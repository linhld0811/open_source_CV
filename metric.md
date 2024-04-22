
## Metric:
1. Reference Quality assessment
- **PSNR(&#8593;) Peak Signalto-Noise Ratio**: metric to measure the similarity between the generated video frames and the ground truth frames <br>
- **LPIPS(&#8595;) - Learned Perceptual Image Patch Similarity** - [Code](https://github.com/richzhang/PerceptualSimilarity)<br>
- **SSIM(&#8593;) - Structure Similarity**: assesses the structural similarity between the generated and ground truth frames by considering luminance, contrast, and structural information <br>
- **FID(&#8595;) - Frechet Inception Distance** - [Code](https://github.com/Po-Hsun-Su/pytorch-ssim): measures the distance between the feature representations of the generated and real video frames extracted from a pre-trained Inception network <br>
- **MS-SSIM(&#8593;) - Multi-Scale Structure Similarity** <br>
- **CSIM(&#8593;) - Cosine Similarity**: evaluate identity preservation in the frames that have been generated. <br>
2. No Reference Quality Assessment
- **NIQE(&#8595;) - Natural Image Quality Evaluator**
- **BRISQUE(&#8595;)- Blind/Referenceless Image Spatial Quality Evaluator**
- **IS - Inception Score**: assesses the quality and diversity of the generated images by leveraging the output of a pre-trained Inception network. <br>
- **Standard Deviation of Head Motion Feature Embeddings(&#8593;)**: assesses the diversity of the generated head motions. extracted from the generated frames using Hopenet <br>
- **CPBD(&#8593;) - Cumulative Probability Blur Detection**: assess image quality by detecting blur. <br>
- **FVD(&#8595;) - Fréchet Video Distance**: evaluate the generated video quality
3. Synchronization Assessment
- **LSE-D(&#8595;) - Lip Shape Evaluation - Distance Score**: evaluates the perceptual differences in lip shape between the generated frames and a reference method <br>
- **LSE-C(&#8593;) - Lip Shape Evaluation - Confidence Score/ Lip Sync Error - Confidence**: assesses the confidence in the generated lip shapes. It represents the confidence score associated with the lip shape generation. <br>
- **LMD(&#8595;) - Landmark Distance**:  evaluate whether the synthesized video corresponds to accurate lip movements based on the input audio <br>
- **AUE- Action Units Error**
- **Beat Align Score(&#8593;)**: used to evaluate the alignment between the audio and the generated head motions. represents a score that quantifies the synchronization of beats between the audio and the generated head motions. <br>
- **CAPP(&#8593;) - Contrastive Audio and Pose Pretraining**: using pose sequence encoder and an audio sequence encoder and predict whether the input pose sequence and audio are paired <br>
- **Sc(&#8593;) & Sd(&#8595;)-confidence score and feature distance extract from Syncnet** - [Code](https://github.com/joonson/syncnet_python): assess the alignment of the input audio with the generated lip movements in videos
