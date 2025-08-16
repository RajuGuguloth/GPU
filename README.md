CUDA Accelerated Image & Graph Algorithms

High-performance CUDA implementations for:

Image processing: 2D convolution (with shared memory tiling) and grayscale transforms

Graph algorithms: Dijkstra, Bellman–Ford, Kruskal (zone-based routing variants)

Profiling & benchmarking: Nsight Systems/Compute and C++ chrono

Achieved 10–15× CPU speedups via shared memory, memory coalescing, warp-level parallelism, and occupancy-aware kernels.

Features

2D Convolution

Tiled shared-memory kernel with halo loading

Coalesced global loads, reduced bank conflicts

Configurable filter sizes (e.g., 3×3, 5×5, 7×7), strides, and padding

Grayscale Transforms

Luma, average, and custom-weighted transforms

Batched images

Parallel Graph Algorithms (Zone-Based Routing)

Dijkstra (priority-queue variants on CPU; frontier-style on GPU)

Bellman–Ford (edge-parallel relaxations)

Kruskal (parallel sort + union-find with path compression)

Optional zone constraints (penalties/forbidden edges)

Benchmarks & Profiling

Built-in timers (std::chrono)

Nsight Systems/Compute recipes and metrics# GPU
