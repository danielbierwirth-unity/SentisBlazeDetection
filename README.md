# WebGL - Real-time Neural Network Inference for Hand and Pose Detection using WebGPU
Neural network inference with models for hand, face, and pose detection provides a more powerful, efficient, and adaptable approach compared to many traditional methods that rely on depth sensing or basic image processing techniques. Traditional methods often require depth-sensing hardware like LiDAR or structured light sensors, and rely heavily on manual image processing techniques such as those provided by OpenCV. These methods can be computationally intensive, less effective in complex scenarios, and limited by hardware and environmental constraints.

Try yourself: [WebGL](https://danielbierwirth-unity.github.io/SentisBlazeDetection/)

In contrast, pre-trained neural networks such as the Google Blaze models allow for streamlined development and real-time detection without needing to code complex processing techniques or use additional depth-sensing hardware. This approach not only reduces the development time but also allows for the fine-tuning of models for specific applications, minimizing the need for extensive datasets.

## Alternative Approaches
Depth sensing devices rely on specialized hardware that may not be available on all devices. They operate using LiDAR or structured light sensors, which are subject to environmental constraints such as reflective surfaces and natural lighting interference.
Traditional image processing techniques, such as those provided by OpenCV, involves extensive manual work for feature extraction and image processing tasks. This approach can be computationally intensive and less effective on resource-constrained devices, making it difficult to handle diverse and complex scenarios efficiently.
Unity Sentis - A Neural Network Inference Library for Unity
Unity Sentis is a powerful neural network inference library designed specifically for Unity. By utilizing this library, developers can import trained neural network models and run them in real-time using end-user device hardware (either GPU or CPU) on supported Unity platforms. This allows for the integration of advanced detection capabilities without the need for extensive expertise in computer vision or the requirement for specialized hardware.
## About the Demo
The demo showcases the capabilities of the Google MediaPipe Blaze models in ONNX Sentis format for real-time detection of hands, faces, and whole body poses in incoming CCTV streams. Using the Unity Sentis API, the models execute asynchronous inference on the GPU via Unity 6 WebGPU directly in the browser.

[\[Link to Video\]](https://youtu.be/mnUTlVGMDaU)

### Utilized Blaze Models
BlazeHand Detector and BlazeHand Landmarker Models: Detects a hand in an image with 33 key points in the camera stream, which can be used to control a hand bone rig.
BlazeFace Model: A fast, light-weight face detector that recognizes faces using a bounding box and six key points.
BlazePose Detector and BlazePose Landmarker Models: Detects whole body poses using 21 key points.

### Execution of Model Inference
The models execute at runtime on incoming webcam image streams directly in the browser, utilizing WebGPU. This design shift the neural network computation from the main CPU thread to the GPU, thus optimizing performance and freeing up the CPU for other tasks.
GPU Compute Shader Integration
Unity 6 supports access to the WebGPU backend in early access, and Sentis leverages this capability to run models effectively on the web using the WebGPU backend. The input tensor operates as part of a GPU compute shader and receives inputs from the webcam texture, facilitating real-time analysis and detection.

### Conclusion
By utilizing pre-trained neural network models and the Unity Sentis API, developers can achieve real-time hand, face, and pose detection in web environments efficiently. This approach enhances development flexibility, reduces the reliance on specialized hardware, and leverages the computing power of GPUs for optimized performance in complex and dynamic scenarios.

#WebGPU #WebGL #NeuralNetworks #AI #Unity3D #MadeWithUnity
