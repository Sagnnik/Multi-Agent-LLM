# Multi-Agent-LLM
The fist upload is a [2-Agent-System](https://github.com/Sagnnik/Multi-Agent-LLM/blob/main/2-agent.ipynb). It is made up of a MANAGER and a CODER. The Task that is given to the MANAGER is wrapped with a json and sent to the CODER. There is a history variable to track the conversation history which is not being used currently. The generated code is then parsed and executed on the notebook itself.  
This is not a practical solution as demostrated in the example when it is asked to set a meet and the time is given but not the person it takes 'John Doe' as the name and generates the code.  

### Current Problems
- It does not have any form of Error Handling
- There could be errors in the user input, generated code as well as the execution output of the code
- The system needs to keep the conversation going while solving the issues

### Possible Solutions
- Make a 3rd Agent like critic that could validate the user input and the generated code output
- This critic should have access to the entire context
- Summarization and context truncation needs to be handeled as well for longer conversation (>3000 tokens)
- For the execution side there needs to be a feedback agent/harcoded condtion (not sure)

### Models Used
I have chosen smaller open source models so that it can be run on google colab easily
- [Phi-3-Mini-4k-Instruct](https://huggingface.co/microsoft/Phi-3-mini-4k-instruct)
- [Qwen2.5-Coder-1.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-Coder-1.5B-Instruct)
