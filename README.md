# 2023 ADL HW3
Author: 栗漢文  r11922191 

## Training
1. Make sure the datas like train.json, public_test.json are already locate in `./data/`
2. Train the qlora model by:
   ``` shell
   sudo bash ./train.sh
   ```
   The train.sh contains only one step:
   * run qlora_train.py to train a peft model
   The hyper-parameters in train.sh can be modified  
   The model will locate in `./output`

## Testing
1. Download the model I trained by:
   ``` shell
   sudo bash ./download.sh
   ```
   The model will locate in  `./adapter_checkpoint`
2. Test the model by:
   ``` shell
   sudo bash ./run.sh /path/to/Taiwan-Llama /path/to/adapter_checkpoint/under/your/folder /path/to/input /path/to/output
   ```
   It will produce a prediction file in /path/to/output
## Others
1. For the learning curve in Q1, I simply copy the training loss raw data in the command line while training.  
2. For the Q2, run_Q2.sh, qlora_test_Q2.py and utils_Q2.py are associated.
