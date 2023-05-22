### Install
Pytorch lightning version:
```
~/miniconda3/envs/mld/bin/pip install pytorch_lightning==1.8.6 --force-reinstall
~/miniconda3/envs/mld/bin/pip install  "torchmetrics<0.7" --force-reinstall
```

### Run
Set DEVICE: [0,1,2,3] (cannot use only 1 gpu???)
```/home/epinyoan/git/motion-latent-diffusion/configs/config_mld_humanml3d.yaml``` 
<br>
<br>
Set Pretrain TEST: CHECKPOINTS: /home/epinyoan/git/motion-latent-diffusion/checkpoints/mld_humanml3d_checkpoint/1222_mld_humanml3d_FID041.ckpt # Pretrained model path


#### Demo
```
python demo.py --cfg ./configs/config_mld_humanml3d.yaml --cfg_assets ./configs/assets.yaml --example ./demo/example.txt
```

```
wandb login
```


### Train MLD
```
python -m train --cfg configs/config_mld_humanml3d.yaml --cfg_assets configs/assets.yaml --batch_size 64 --nodebug
```