Vulkan Engine

<video src="https://github.com/user-attachments/assets/6d6f6881-995d-4e77-b41b-000bc6e5da42" autoplay loop muted playsinline width="100%"></video>

  • Swap chains and presentation modes.
  
  • Swap chain cleanup and recreation for image view changes.
  
  • Syncing CPU and GPU using fences so CPU can work on the next frame while the GPU is busy to minimize CPU idle time.
  
  • Syncing GPU queue families using semaphores with (image available semaphore and render finished semaphore pair for
  each frame).
  
  • Uniform Buffer Object for manipulating model, view, projection matrices achieving movement with consistent camera view.
