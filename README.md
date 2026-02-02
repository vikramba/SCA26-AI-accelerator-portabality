# SCA26-AI-accelerator-portabality

| Platform | Primary Hardware | Software Stack/Ecosystem | Framework Support | Programming Model/APIs | Architecture Type | Deployment/Inference Tools | Key Portability Strategy | Best Use Case |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **NVIDIA** | H100 (Hopper), B200 (Blackwell) | CUDA, cuDNN, TensorRT, Transformer Engine | PyTorch, TensorFlow, JAX, Keras, MXNet | SIMT, CUDA Kernels, Triton | Parallel Cores (Tensor Cores) | TensorRT, TensorRT-LLM, vLLM | Triton (cross-vendor kernels), PyTorch Inductor, ONNX | Frontier Model Training, risk-averse enterprise workloads |
| **Google TPU** | TPU v5p, Trillium (v6e) | XLA, PJRT, OpenXLA | JAX (Native), TensorFlow (Native), PyTorch/XLA | SPMD, Pallas (custom kernels) | Systolic Arrays (MXU) | Triton (exp), Cloud TPU APIs | OpenXLA/StableHLO, PJRT runtime | Massive-scale foundation model training, Cloud-native efficiency |
| **AMD** | Instinct MI300X, MI325X | ROCm, HIP, hipBLAS, MIOpen | PyTorch (native), TensorFlow, JAX (plugin) | SIMT, HIP, Triton | Parallel Cores (Matrix Cores / CDNA) | vLLM, MIGraphX | HIP (source translation), Triton backend, ZLUDA | High-volume/high-throughput inference (70B+), cost-efficient scaling |
| **Intel** | Gaudi 3, Data Center GPU Max | oneAPI, oneDNN, oneMKL, DPC++ | PyTorch (xpu), TensorFlow (Extension) | SYCL (standard C++), Triton (XPU) | Systolic Arrays (MME) and TPC | OpenVINO | oneAPI (SYCL), joint_matrix API, Integrated RoCE | Enterprise on-premise AI clusters, mid-range TCO-focused deployment |
