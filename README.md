# pipeline_paddle_viton

To run

Step 1: git clone https://github.com/ANAGHA-20/pipeline_paddle_viton
Step 2: %cd ./pipeline_paddle_viton
Step 3: pip install -r requirements.txt
        pip install paddlepaddle-gpu
        pip install pymatting
        import os
Step 4: export CUDA_VISIBLE_DEVICES=0
Step 5: wget "https://paddleseg.bj.bcebos.com/matting/models/ppmatting-hrnet_w18-human_1024.pdparams" -O "/content/pipeline_paddle_viton/models/ppmatting-hrnet_w18-human_1024.pdparams"
Step 6: run

!python bg_replace.py \
    --config configs/ppmatting/ppmatting-hrnet_w18-human_1024.yml \
    --model_path models/ppmatting-hrnet_w18-human_1024.pdparams \
    --image_path ./image/person.jpg \
    --save_dir ./output \
    --fg_estimate True
