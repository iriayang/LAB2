# Demo Usage


## Inference on a image folder

The command line should be like this:
```shell
    python demo/demo.py base configs/vid_R_101_C4_1x.yaml R_101.pth --suffix ".JPEG"
        --visualize-path /datasets/image_folder
        --output-folder visualization [--output-video]

```
This will generate visualization result using single frame baseline with ResNet-101 backbone. And the results, images with generated bboxes, are saved in folder `visualization`. 


## Inference on a video

The command line should be like this for base:
```shell
 python demo/demo.py base configs/vid_R_101_C4_1x.yaml R_101.pth --video 
    --visualize-path datasets/panda.mp4  
    --output-folder panda --output-video
```

The command line should be like this for mega:
```shell
python demo/demo.py mega configs/MEGA/vid_R_101_C4_MEGA_1x.yaml MEGA_R_101.pth --video 
    --visualize-path datasets/panda.mp4  
    --output-folder panda_MEGA --output-video
```


This will generate visualization result using single frame baseline with ResNet-101 backbone. And the results, images with generated bboxes, are saved in folder `visualization`. 
Change the name of the folder and the video that you are using


