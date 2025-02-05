# VLLM Runner Utils

This script runs the vllm_runner module with the specified checkpoint, input text file, and output text file.
The '--tp' flag is used to set the number of tensor parallelism (TP) to 2.
Usage:
```bash
python -m vllm_runner.run <checkpoint_path> <input_text_path> <output_text_path> --tp <tensor_parallelism>
```

## Expected Input Format
The input should be a JSON file named `input.json` with the following structure:
```json
{
    "texts": [
        "text1",
        "text2",
        "text3"
    ]
}
```

## Expected Output Format
The output should be a JSON file named `output.pt` with the following structure:
```json
{
    "text1": "embedding1",
    "text2": "embedding2",
    "text3": "embedding3"
}
```
