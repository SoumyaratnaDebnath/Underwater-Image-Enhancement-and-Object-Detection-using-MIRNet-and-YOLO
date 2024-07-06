# Underwater Image Enhancement and Object Detection using MIRNet and YOLO

### Abstract

<p style="text-align:justify;">With the goal of recovering high-quality image content from its degraded version, image restoration finds numerous applications in fields such as surveillance, computational photography, medical imaging, and remote sensing. Recently, convolutional neural networks (CNNs) have significantly improved the image restoration process. Conventional CNN-based methods typically operate either on full-resolution or progressively low-resolution representations. While the former achieves spatial precision but lacks contextual robustness, the latter provides semantically reliable but spatially less accurate outputs. MIRNet is a novel architecture designed to maintain spatially precise high-resolution representations throughout the network while extracting strong contextual information from low-resolution representations. The core approach involves a multi-scale residual block featuring parallel multi-resolution convolution streams, information exchange across these streams, spatial and channel attention mechanisms, and attention-based multi-scale feature aggregation. This approach learns enriched features that combine contextual information from multiple scales while preserving high-resolution spatial details. The source code and pre-trained models are available at the MIRNet repository: https://github.com/swz30/MIRNet.</p>

### Introduction

<p style="text-align:justify;">Image restoration and enhancement are critical tasks in computer vision, aimed at recovering high-quality images from degraded inputs. Applications of these tasks span across various fields including surveillance, computational photography, medical imaging, and remote sensing. Traditional image restoration pipelines often utilize either full-resolution processing or encoder-decoder architectures. While full-resolution processing retains precise spatial details, encoder-decoder architectures offer better contextual representations. However, these methods fail to satisfy both requirements simultaneously, which is essential for real-world image restoration tasks.</p>

### Methodology

#### MIRNet Architecture

<p style="text-align:justify;">MIRNet introduces a novel architecture that integrates the benefits of both full-resolution processing and multi-scale feature extraction. The main branch of MIRNet is dedicated to full-resolution processing, ensuring spatial precision. Complementary parallel branches provide enhanced contextual features. The architecture employs multi-scale residual blocks containing several key elements: parallel multi-resolution convolution streams for multi-scale feature extraction, information exchange across these streams, spatial and channel attention mechanisms to capture contextual information, and attention-based multi-scale feature aggregation.</p>

#### Multi-Scale Residual Block

<p style="text-align:justify;">The multi-scale residual block is the cornerstone of MIRNet's architecture. It extracts features at multiple scales through parallel convolution streams, allowing the network to capture both fine details and broader contextual information. Information exchange across these streams ensures a comprehensive understanding of the image, while spatial and channel attention mechanisms highlight relevant features, facilitating effective feature aggregation and improved restoration quality.</p>

### Implementation

#### Full-Resolution and Multi-Scale Processing

<p style="text-align:justify;">MIRNet processes the image in full resolution through its main branch, retaining spatial details. Simultaneously, parallel branches operate at multiple scales, capturing contextual information. The integration of features from these branches results in a comprehensive restoration approach that combines spatial precision with contextual robustness.</p>

#### Attention Mechanisms

<p style="text-align:justify;">Spatial and channel attention mechanisms play a crucial role in MIRNet's architecture. These mechanisms enable the network to focus on important regions and features within the image, enhancing the overall restoration process. By leveraging attention mechanisms, MIRNet can effectively combine multi-scale features, resulting in high-quality restored images.</p>

### Results and Discussion

<p style="text-align:justify;">MIRNet's architecture demonstrates significant improvements in image restoration and enhancement tasks. By combining full-resolution processing with multi-scale feature extraction, the network achieves a balance between spatial precision and contextual robustness. The attention mechanisms further enhance the restoration quality, ensuring high-resolution details and enriched contextual information.</p>

![](Enhancement-Samples.png)

### YOLO Object Detection

<p style="text-align:justify;">YOLO, an abbreviation for 'You Only Look Once,' is a cutting-edge algorithm designed for real-time object detection and recognition. By treating object detection as a regression problem, YOLO predicts class probabilities and bounding boxes with a single forward pass through a convolutional neural network (CNN). This approach enables YOLO to perform object detection efficiently and accurately, making it a preferred choice for various applications in computer vision.</p>

### Methodology

#### YOLO Architecture

<p style="text-align:justify;">YOLO's architecture processes the entire image in a single pass, dividing it into an \(N \times N\) grid. For each grid cell, YOLO predicts multiple bounding boxes and class probabilities. This fully convolutional approach contrasts with traditional region proposal networks, which require multiple predictions for various regions in the image. YOLO's single-pass method significantly enhances detection speed and efficiency.</p>

#### Regression Approach

<p style="text-align:justify;">By reframing object detection as a regression problem, YOLO maps image pixels directly to bounding box coordinates and class probabilities. This global reasoning allows YOLO to capture contextual information about object classes and appearances, reducing background errors and improving detection accuracy. The network's ability to reason globally about the image context enhances its performance compared to traditional methods.</p>

### Benefits of YOLO

#### Speed and Efficiency

<p style="text-align:justify;">YOLO's primary advantage is its speed. By processing the image in a single pass, YOLO can perform real-time object detection, making it suitable for applications requiring fast response times. The simplified detection pipeline further enhances efficiency, allowing the algorithm to handle high-resolution images and complex scenes effectively.</p>

#### Global Reasoning

<p style="text-align:justify;">YOLO's global reasoning capability leads to more accurate predictions. Unlike sliding window and region proposal-based techniques, YOLO considers the entire image context during both training and testing. This comprehensive approach reduces background errors and improves object localization, enabling YOLO to differentiate objects from their surroundings more effectively.</p>

#### Generalization

<p style="text-align:justify;">YOLO excels in learning generalizable representations of objects. When trained on natural images, YOLO outperforms other top detection methods, such as DPM and R-CNN, in diverse domains, including artwork. This robust generalization capability ensures that YOLO performs well even when applied to new and unexpected inputs, making it a versatile tool for various object detection tasks.</p>

### Results

<p style="text-align:justify;">YOLO utilizes features from the entire image to predict each bounding box and class probability simultaneously. This design allows the network to maintain high average precision while achieving real-time detection speeds. The ability to train and optimize on full images directly enhances the overall detection performance.</p>

![](Detection-Samples.png)

### Dataset Description

<p style="text-align:justify;">For training YOLO, the Brackish Underwater Dataset is utilized. This dataset is the first publicly available European underwater image dataset with bounding box annotations of fish, crabs, and other marine organisms. Recorded in Limfjorden, a brackish strait in northern Denmark, the dataset offers a unique set of underwater images captured using a camera setup consisting of three cameras and three LED lights mounted on a concrete pillar of the Limfjords bridge. Currently, only data from one camera has been annotated and published, with more expected to be added. The setup, located 9 meters below the surface, operates with a single LED light during recordings, influencing the behavior of marine animals, such as the schooling of sticklebacks directly in front of the camera.</p>

### Conclusion

<p style="text-align:justify;">YOLO stands out as a groundbreaking object detection algorithm that combines speed, accuracy, and generalization. By treating object detection as a regression problem and leveraging a fully convolutional neural network, YOLO simplifies the detection process while enhancing performance. The use of the Brackish Underwater Dataset for training highlights YOLO's applicability to diverse environments and its potential for various real-world applications. The algorithm's ability to perform real-time detection with high precision makes it a valuable tool in the field of computer vision.</p>

### Future Work

<p style="text-align:justify;">Future improvements to YOLO could involve refining the network architecture to enhance detection accuracy and speed further. Exploring additional datasets and domains will also help validate and extend YOLO's capabilities. Integrating more advanced techniques, such as attention mechanisms and multi-scale feature extraction, could further boost the algorithm's performance in complex scenarios.</p>
