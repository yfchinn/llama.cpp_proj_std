## Name : 111550126金以凡

### Basic Challenge
| Throughputs (Tokens/sec) | CPU      | GPU      | 
| --------                 | -------- | -------- | 
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf  | 10.22     | 108.43     |


### Medium Challenge
| Throughputs (Tokens/sec) | CPU      | GPU      | 
| --------                 | -------- | -------- | 
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf  | 10.22     | 108.43     |
| TinyLlama-1.1B-Chat-v1.0-f16  | 5.36     | 73.61     |



### Advance Challenge
| Throughputs (Tokens/sec) | CPU      | GPU      | 
| --------                 | -------- | -------- | 
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf  | 10.22     | 108.43     |
| TinyLlama-1.1B-Chat-v1.0-f16  | 5.36     | 73.61     |
| TinyLlama-1.1B-Chat-v1.0-Q8  | 5.78     | 87.43     |


### Advance Challenge

| Throughputs (Tokens/sec) | Accuracy  |
| --------                 | --------  |
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf | 1/10     |
| TinyLlama-1.1B-Chat-v1.0-f16         | 2/10     |
| TinyLlama-1.1B-Chat-v1.0-Q8          | 5/10     |

### Questions
* What problems you encountered? How you solve it?  
  Ans: Don't know how to determine whether the GPU or CPU is currently being used during model inference. It can be solved by checking "offloaded 0/23 layers to GPU".
* What you observed between CPU / GPU performance?  
  Ans: In terms of performance, GPU is about 10 times faster than CPU.
* Will quantization or smaller-parameters model impact model accuracy or inference throughput? If so, what's the variation?  
  Ans: Yes. The smaller-parameters model has lower accuracy and higher throughput.  
  Experimental data shows:
   * Throughput: Q4 > Q8 > f16
   * Accuracy: Q8 > f16 > Q4 (contrary to the initial expectation of f16 > Q8 > Q4)



