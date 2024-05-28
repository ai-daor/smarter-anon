To run training and eval (need at least 40GB mem, 166 cores, and preferably a V100 GPU):

```
conda create --name smarter python=3.10
conda activate smarter
pip install -r requirements.txt

python main_reasoner.py --model_name fused_dinov2_siglip --log --word_embed siglip --save_root final_runs --data_root <SMART101_data_path> --lr 0.0003 --wd 0.2 --batch_size 128 --num_heads 2 --repr_size 128 --qf_layer --eps 1e-8 --beta2 0.98 --pdrop 0.2 --ln_eps 1e-6 --h_sz 256 --seed 0 --num_workers 16 
```

To download the SMART101 dataset (from [merl](https://github.com/merlresearch/SMART)), please execute the get_SMART_data.sh script in the repository. 


