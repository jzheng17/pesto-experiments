# Quick Guide for Pesto Model Training
## On Mac:
1. Create a folder named `data` in project root dir: `mkdir ./data`
2. Download MIR-1k from kaggle and put it inside this folder.
3. Generate csv file: 
   ```shell
   find MIR-1K/Vocals -name "*.wav" | sort > mir-1k.csv
   find MIR-1K/PitchLabel -name "*.pv" | sort > mir-1k_annot.csv
   ```
4. Start training!
   ```shell
   python src/train.py data=mir-1k logger=csv
   ```
   - Optionally, on mac you may add `trainer=mps` or `trainer=cpu` 