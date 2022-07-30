# pipeline_paddle_viton

To run

<br> Step 1: git clone https://github.com/ANAGHA-20/pipeline_paddle_viton
<br> Step 2: %cd ./pipeline_paddle_viton
<br> Step 3: pip install -r requirements.txt
<br>         pip install paddlepaddle-gpu
<br>         pip install pymatting
<br>         import os
<br> Step 4: export CUDA_VISIBLE_DEVICES=0
<br> Step 5: wget "https://paddleseg.bj.bcebos.com/matting/models/ppmatting-hrnet_w18-human_1024.pdparams" -O "/content/pipeline_paddle_viton/models/ppmatting-hrnet_w18-human_1024.pdparams"
<br> Step 6: run
<br> 
!python bg_replace.py \
    --config configs/ppmatting/ppmatting-hrnet_w18-human_1024.yml \
    --model_path models/ppmatting-hrnet_w18-human_1024.pdparams \
    --image_path ./image/person.jpg \
    --save_dir ./output \
    --fg_estimate True
