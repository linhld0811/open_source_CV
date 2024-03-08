Talking head generation:
GAN/cGANs
attention

Category:
- image-driven
- video-driven
- NeRF + 3D
- audio-driven
Input:
text/audio + facical expression

<h2>Metric</h2>:
<h3>Quality</h3>:
- PSNR: metric to measure the similarity between the generated video frames and the ground truth frames
- SSIM: assesses the structural similarity between the generated and ground truth frames by considering luminance, contrast, and structural information
- Cosine Similarity (CSIM): CSIM is employed to evaluate identity preservation in the frames that have been generated.
- FID: measures the distance between the feature representations of the generated and real video frames extracted from a pre-trained Inception network
- Inception Score (IS): assesses the quality and diversity of the generated images by leveraging the output of a pre-trained Inception network.
- Cumulative Probability Blur Detection (CPBD): assess image quality by detecting blur. 
- Lip Shape Evaluation - Distance Score (LSE-D): evaluates the perceptual differences in lip shape between the generated frames and a reference method
- Lip Shape Evaluation - Confidence Score (LSE-C): assesses the confidence in the generated lip shapes. It represents the confidence score associated with the lip shape generation.
- Standard Deviation of Head Motion Feature Embeddings: assesses the diversity of the generated head motions. extracted from the generated frames using Hopenet
- Beat Align Score: used to evaluate the alignment between the audio and the generated head motions. represents a score that quantifies the synchronization of beats between the audio and the generated head motions.
- Landmark Distance(LMD):  evaluate whether the synthesized video corresponds to accurate lip movements based on the input
audio

Pros: commonly used to assess the quality
Cons:
- May not capture the perceptual realism and naturalness of the synthesized faces accurately
- Focus primarily on pixel-level similarityand do not account for higher-level visual cues such as facial expressions, lip movements, and overall coherence in speech animation

Desired properties:
- preserving the subject’s original identity: cosine similarity between embedding vectors of ArcFace to measure identity mismatch.
- maintaining lip-sync at a semantic level: Using SSIM and FID to evaluate visual quality at an image-level, and CPBD to judge the sharpness of the synthesized video.
- keeping high visual quality
- containing spontaneous motions

Loss:
- Recontruction Loss
- Adversarial Loss
- Perceptual Loss
- Temporal Coherence Loss


luminance, contrast, and structural information
identity preservation
high visual quality
spontaneous motions
facial expressions, lip movements, synchronization of beats between the audio and the generated head motions
speaking style, identity-dependent facial shape
pose(head, jaw, and eyeball rotations)


Audio/speech-driven:
Lips synced: /Wav2Lip(2020)/AD-AVR(2019)
- learn mapping audio and visual
Synthesizing obama(2017): audio -(RNN)-> sparse shape -(mouth synthesis)-> mouth texture(photo-realistic) -(re-timing)-> target video -(Final composite)-> final video
LMGG(2019): 
audio -(audio encoder)->    audio features   + -> video features -(decoder)-> video
image -(identity encoder)-> visual features /
Wav2Lip(2020):
https://github.com/Rudrabha/Wav2Lip
audio + video -> expert lip-sync discriminator (SyncNet) -> penalize generator(LipGAN): Speech encoder + identity encoder + face decoder + visual quality discriminator
Wav2LipHD: Wav2Lip + Real-ESRGAN
https://github.com/saifhassan/Wav2Lip-HD
TalkLip(2023):
https://github.com/Sxjdwang/TalkLip
SyncTalk(2024):
https://github.com/ZiqiaoPeng/SyncTalk
Video-retalking(2023): 
https://github.com/OpenTalker/video-retalking
HyperLips:
https://github.com/semchan/HyperLips
StyleSync:
https://github.com/guanjz20/StyleSync_PyTorch
StyleTalk: 
https://github.com/FuxiVirtualHuman/styletalk
GenFace++:
https://github.com/yerfor/GeneFacePlusPlus
Real3DPortrait:
https://github.com/yerfor/Real3DPortrait
DreamTalk:
https://github.com/ali-vilab/dreamtalk

Facial and Head movements: EmoGen(2023) https://github.com/sahilg06/EmoGen
Disentangled Modalities: Styletalker(2023)

SadTalker: https://github.com/OpenTalker/SadTalker
https://github.com/wangsuzhen/Audio2Head
https://github.com/LizhenWangT/StyleAvatar
https://github.com/EvelynFan/FaceFormer (2020)
https://github.com/IDEA-Research/LipsFormer (2023)
https://github.com/TimoBolkart/voca
https://github.com/sstzal/DiffTalk 2023

face-alignment:
https://github.com/deepinsight/insightface
https://github.com/1adrianb/face-alignment


https://github.com/RenYurui/PIRender
