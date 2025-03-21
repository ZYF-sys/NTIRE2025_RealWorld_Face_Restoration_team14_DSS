The download link for the checkpoints can be found in `/model_zoo/team14_DSS/team14_DSS.txt`.
The model also has been uploaded to HuggingFace. You can use the following commands to clone the entire model directory.:
``` 
git lfs install
git clone https://huggingface.co/Zmund/team14_DSS
```

The checkpoints consist of the following directories. Please download the entire directory:
team14_DSS
    ├── diffbir
    ├── stablesr
    ├── supir

Due to the program's requirements, please modify line 27 of test.py to use the model's **absolute path** as follows:
`model_path = os.path.join('/root/autodl-tmp/', 'team14_DSS')`

To execute the program, you can use the following command (ensure the terminal is in the same directory as test.py):
`python test.py --test_dir /path/to/test --save_dir /path/to/save --model_id 1`

In this command:
Replace /path/to/test with the path to your test files.
Replace /path/to/save with the directory where you want to save the output.
1 is the model ID to be used.