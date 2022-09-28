# yolov5_v6_plate_heading

+ 集成yolov5(v6.0), yolox, 注意力机制， 和repvgg结构  
+ 添加了多头检测代码，使用train_plate.py文件进行训练

```bash
$ python train_plate.py --data data/mydata.yaml --batch 256 --epochs 200 --weights weights/yolov5s.pt   --imgsz 416  --device '0,1'  --cfg models/yolov5s_plate.yaml  --hyp data/hyps/palte_head.yaml 
```

 If you use multi-gpu. It's faster several times:
  
 ```bash
$ python -m torch.distributed.launch --nproc_per_node 2 train_plate.py --sync-bn
```