# Reproducing Results from the paper

## Environment Details

```bash
Python version: 3.8.12 (default, Oct 12 2021, 13:49:34) 
[GCC 7.5.0]
PyTorch version: 1.11.0
CUDA version: 11.3
```

## Results  `ImageNet-A`

<!-- <style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-lqy6{text-align:right;vertical-align:top}
.tg .tg-amwm{font-weight:bold;text-align:center;vertical-align:top}
.tg .tg-fymr{border-color:inherit;font-weight:bold;text-align:left;vertical-align:top}
.tg .tg-dvpl{border-color:inherit;text-align:right;vertical-align:top}
</style> -->
<table class="tg">
<thead>
  <tr>
    <th class="tg-amwm">ImageNet-R</th>
    <th class="tg-amwm">Run-1</th>
    <th class="tg-amwm">Run-2</th>
    <th class="tg-amwm">Paper</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-fymr">ResNet-50</td>
    <td class="tg-dvpl">100.0</td>
    <td class="tg-dvpl">100.0</td>
    <td class="tg-lqy6">100.0</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">99.9</td>
    <td class="tg-dvpl">99.8</td>
    <td class="tg-lqy6">99.1</td>
  </tr>
  <tr>
    <td class="tg-fymr">DeepAug+AugMix</td>
    <td class="tg-dvpl">96.1</td>
    <td class="tg-dvpl">96.1</td>
    <td class="tg-lqy6">96.1</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">95.5</td>
    <td class="tg-dvpl">95.6</td>
    <td class="tg-lqy6">94.8</td>
  </tr>
  <tr>
    <td class="tg-fymr">MoEx+CutMix</td>
    <td class="tg-dvpl">92.0</td>
    <td class="tg-dvpl">92.0</td>
    <td class="tg-lqy6">91.9</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">91.5</td>
    <td class="tg-dvpl">91.4</td>
    <td class="tg-lqy6">89.0</td>
  </tr>
</tbody>
</table>


### Logs for `ImageNet-A`
<details>
    <summary>Click me</summary>



**Log for Run 1**

```bash
$ ./script__imagenet_a.sh

adversarial level 0
Resuming from results/imagenet_rn50/...
Test: [ 0/30]   Time 10.343 (10.343)    Acc@1   0.00 (  0.00)
Test: [10/30]   Time  0.169 ( 1.095)    Acc@1   0.00 (  0.00)
Test: [20/30]   Time  0.238 ( 0.659)    Acc@1   0.00 (  0.00)
 * Acc@1 0.000
Error on corrupted test set 100.00
Resuming from results/imagenet_rn50/...
Running...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7500/7500 [3:12:39<00:00,  1.54s/it]
MEMO adapt test error 99.87


adversarial level 0
Resuming from results/imagenet_rn50_daam/...
Test: [ 0/30]   Time 12.296 (12.296)    Acc@1   0.07 (  0.07)
Test: [10/30]   Time  0.171 ( 1.274)    Acc@1   0.04 (  0.05)
Test: [20/30]   Time  0.171 ( 0.780)    Acc@1   0.01 (  0.05)
 * Acc@1 0.039
Error on corrupted test set 96.13
Resuming from results/imagenet_rn50_daam/...
Running...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7500/7500 [2:57:59<00:00,  1.42s/it]
MEMO adapt test error 95.48


adversarial level 0
Resuming from results/imagenet_rn50_moex/...
Test: [ 0/30]   Time 12.456 (12.456)    Acc@1   0.09 (  0.09)
Test: [10/30]   Time  0.171 ( 1.288)    Acc@1   0.09 (  0.11)
Test: [20/30]   Time  0.170 ( 0.779)    Acc@1   0.05 (  0.09)
 * Acc@1 0.080
Error on corrupted test set 92.03
Resuming from results/imagenet_rn50_moex/...
Running...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7500/7500 [2:51:38<00:00,  1.37s/it]
MEMO adapt test error 91.47
```


**Log for Run 2**

```bash
$ ./script__imagenet_a.sh

adversarial level 0
Resuming from results/imagenet_rn50/...
Test: [ 0/30]   Time 13.984 (13.984)    Acc@1   0.00 (  0.00)
Test: [10/30]   Time  0.171 ( 1.427)    Acc@1   0.00 (  0.00)
Test: [20/30]   Time  0.633 ( 0.868)    Acc@1   0.00 (  0.00)
 * Acc@1 0.000
Error on corrupted test set 100.00
Resuming from results/imagenet_rn50/...
Running...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7500/7500 [2:49:35<00:00,  1.36s/it]
MEMO adapt test error 99.84


adversarial level 0
Resuming from results/imagenet_rn50_daam/...Test: [ 0/30]   Time 11.775 (11.775)    Acc@1   0.07 (  0.07)Test: [10/30]   Time  0.171 ( 1.227)    Acc@1   0.04 (  0.05)
Test: [20/30]   Time  0.355 ( 0.749)    Acc@1   0.01 (  0.05)
 * Acc@1 0.039
Error on corrupted test set 96.13
Resuming from results/imagenet_rn50_daam/...
Running...
███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7500/7500 [3:08:54<00:00,  1.51s/it]
MEMO adapt test error 95.63


adversarial level 0
Resuming from results/imagenet_rn50_moex/...
Test: [ 0/30]   Time 12.681 (12.681)    Acc@1   0.09 (  0.09)Test: [10/30]   Time  0.170 ( 1.309)    Acc@1   0.09 (  0.11)Test: [20/30]   Time  0.172 ( 0.792)    Acc@1   0.05 (  0.09)
 * Acc@1 0.080
Error on corrupted test set 92.03
Resuming from results/imagenet_rn50_moex/...
Running...
100%|███████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 7500/7500 [3:24:55<00:00,  1.64s/it]
MEMO adapt test error 91.36
```


</details>


## Results  `ImageNet-R`


<table class="tg">
<thead>
  <tr>
    <th class="tg-amwm">ImageNet-A</th>
    <th class="tg-amwm">Run-1</th>
    <th class="tg-amwm">Run-2</th>
    <th class="tg-amwm">Paper</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-fymr">ResNet-50</td>
    <td class="tg-dvpl">63.8</td>
    <td class="tg-dvpl">63.8</td>
    <td class="tg-lqy6">63.9</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">61.3</td>
    <td class="tg-dvpl">61.3</td>
    <td class="tg-lqy6">58.8</td>
  </tr>
  <tr>
    <td class="tg-fymr">DeepAug+AugMix</td>
    <td class="tg-dvpl">53.2</td>
    <td class="tg-dvpl">53.2</td>
    <td class="tg-lqy6">53.2</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">51.3</td>
    <td class="tg-dvpl">51.3</td>
    <td class="tg-lqy6">49.2</td>
  </tr>
  <tr>
    <td class="tg-fymr">MoEx+CutMix</td>
    <td class="tg-dvpl">64.5</td>
    <td class="tg-dvpl">64.5</td>
    <td class="tg-lqy6">64.5</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">61.8</td>
    <td class="tg-dvpl">61.9</td>
    <td class="tg-lqy6">59.4</td>
  </tr>
</tbody>
</table>


### Logs for `ImageNet-R`

<details>
    <summary>Click me</summary>
    

**Log for Run 1**

```bash
 $ ./script__imagenet_r.sh 

rendition level 0
Resuming from results/imagenet_rn50/...
Test: [  0/118] Time 11.375 (11.375)    Acc@1   0.24 (  0.24)
Test: [ 10/118] Time  0.175 ( 1.193)    Acc@1   0.40 (  0.32)
Test: [ 20/118] Time  0.174 ( 0.756)    Acc@1   0.21 (  0.32)
Test: [ 30/118] Time  0.175 ( 0.662)    Acc@1   0.51 (  0.35)
Test: [ 40/118] Time  0.175 ( 0.596)    Acc@1   0.28 (  0.38)
Test: [ 50/118] Time  0.197 ( 0.550)    Acc@1   0.23 (  0.36)
Test: [ 60/118] Time  0.442 ( 0.546)    Acc@1   0.27 (  0.36)
Test: [ 70/118] Time  0.215 ( 0.525)    Acc@1   0.33 (  0.35)
Test: [ 80/118] Time  0.174 ( 0.494)    Acc@1   0.45 (  0.35)Test: [ 90/118] Time  0.176 ( 0.489)    Acc@1   0.27 (  0.36)Test: [100/118] Time  0.201 ( 0.473)    Acc@1   0.61 (  0.37)
Test: [110/118] Time  0.174 ( 0.465)    Acc@1   0.30 (  0.37)
 * Acc@1 0.362
Error on corrupted test set 63.83
Resuming from results/imagenet_rn50/...
Running...
100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 30000/30000 [10:49:16<00:00,  1.30s/it]
MEMO adapt test error 61.27

rendition level 0
Resuming from results/imagenet_rn50_daam/...Test: [  0/118] Time 10.056 (10.056)    Acc@1   0.37 (  0.37)Test: [ 10/118] Time  0.174 ( 1.072)    Acc@1   0.48 (  0.43)
Test: [ 20/118] Time  0.206 ( 0.647)    Acc@1   0.29 (  0.43)
Test: [ 30/118] Time  0.174 ( 0.520)    Acc@1   0.67 (  0.46)
Test: [ 40/118] Time  0.175 ( 0.459)    Acc@1   0.41 (  0.50)
Test: [ 50/118] Time  0.175 ( 0.429)    Acc@1   0.37 (  0.47)
Test: [ 60/118] Time  0.175 ( 0.405)    Acc@1   0.42 (  0.47)
Test: [ 70/118] Time  0.966 ( 0.395)    Acc@1   0.46 (  0.46)
Test: [ 80/118] Time  0.174 ( 0.375)    Acc@1   0.54 (  0.47)
Test: [ 90/118] Time  0.175 ( 0.363)    Acc@1   0.44 (  0.47)
Test: [100/118] Time  0.186 ( 0.349)    Acc@1   0.74 (  0.48)
Test: [110/118] Time  0.281 ( 0.338)    Acc@1   0.37 (  0.47)
 * Acc@1 0.468
Error on corrupted test set 53.23
Resuming from results/imagenet_rn50_daam/...
Running...
████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 30000/30000 [10:42:19<00:00,  1.28s/it]
MEMO adapt test error 51.29

rendition level 0
Resuming from results/imagenet_rn50_moex/...Test: [  0/118] Time 11.973 (11.973)    Acc@1   0.25 (  0.25)
Test: [ 10/118] Time  0.176 ( 1.248)    Acc@1   0.39 (  0.31)
Test: [ 20/118] Time  0.222 ( 0.779)    Acc@1   0.20 (  0.31)
Test: [ 30/118] Time  0.200 ( 0.672)    Acc@1   0.50 (  0.33)
Test: [ 40/118] Time  0.174 ( 0.582)    Acc@1   0.28 (  0.36)
Test: [ 50/118] Time  0.179 ( 0.534)    Acc@1   0.22 (  0.35)
Test: [ 60/118] Time  0.180 ( 0.506)    Acc@1   0.29 (  0.34)
Test: [ 70/118] Time  1.666 ( 0.511)    Acc@1   0.32 (  0.34)
Test: [ 80/118] Time  0.206 ( 0.484)    Acc@1   0.47 (  0.34)
Test: [ 90/118] Time  0.185 ( 0.471)    Acc@1   0.26 (  0.35)
Test: [100/118] Time  0.176 ( 0.475)    Acc@1   0.64 (  0.37)
Test: [110/118] Time  1.496 ( 0.473)    Acc@1   0.27 (  0.36)
 * Acc@1 0.355
Error on corrupted test set 64.48
Resuming from results/imagenet_rn50_moex/...
Running...
████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 30000/30000 [14:11:08<00:00,  1.70s/it]
MEMO adapt test error 61.77
```


**Log for Run 1**

```bash
 $ ./script__imagenet_r.sh 

rendition level 0
Resuming from results/imagenet_rn50/...
Test: [  0/118] Time 13.149 (13.149)    Acc@1   0.24 (  0.24)
Test: [ 10/118] Time  0.175 ( 1.366)    Acc@1   0.40 (  0.32)
Test: [ 20/118] Time  0.175 ( 0.836)    Acc@1   0.21 (  0.32)
Test: [ 30/118] Time  0.335 ( 0.721)    Acc@1   0.51 (  0.35)
Test: [ 40/118] Time  0.221 ( 0.651)    Acc@1   0.28 (  0.38)
Test: [ 50/118] Time  0.175 ( 0.601)    Acc@1   0.23 (  0.36)
Test: [ 60/118] Time  0.175 ( 0.563)    Acc@1   0.27 (  0.36)
Test: [ 70/118] Time  0.175 ( 0.520)    Acc@1   0.33 (  0.35)
Test: [ 80/118] Time  0.175 ( 0.509)    Acc@1   0.45 (  0.35)
Test: [ 90/118] Time  0.175 ( 0.507)    Acc@1   0.27 (  0.36)
Test: [100/118] Time  0.206 ( 0.483)    Acc@1   0.61 (  0.37)
Test: [110/118] Time  0.312 ( 0.467)    Acc@1   0.30 (  0.37)
 * Acc@1 0.362
Error on corrupted test set 63.83
Resuming from results/imagenet_rn50/...
Running...
100%|████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 30000/30000 [13:11:19<00:00,  1.58s/it]
MEMO adapt test error 61.33

rendition level 0
Resuming from results/imagenet_rn50_daam/...
Test: [  0/118] Time 10.210 (10.210)    Acc@1   0.37 (  0.37)
Test: [ 10/118] Time  0.176 ( 1.087)    Acc@1   0.48 (  0.43)
Test: [ 20/118] Time  0.175 ( 0.654)    Acc@1   0.29 (  0.43)
Test: [ 30/118] Time  0.175 ( 0.520)    Acc@1   0.67 (  0.46)
Test: [ 40/118] Time  0.175 ( 0.461)    Acc@1   0.41 (  0.50)
Test: [ 50/118] Time  0.175 ( 0.434)    Acc@1   0.37 (  0.47)
Test: [ 60/118] Time  0.177 ( 0.409)    Acc@1   0.42 (  0.47)
Test: [ 70/118] Time  0.896 ( 0.397)    Acc@1   0.46 (  0.46)
Test: [ 80/118] Time  0.176 ( 0.378)    Acc@1   0.54 (  0.47)
Test: [ 90/118] Time  0.175 ( 0.367)    Acc@1   0.44 (  0.47)
Test: [100/118] Time  0.176 ( 0.353)    Acc@1   0.74 (  0.48)
Test: [110/118] Time  0.690 ( 0.346)    Acc@1   0.37 (  0.47)
 * Acc@1 0.468
Error on corrupted test set 53.23
Resuming from results/imagenet_rn50_daam/...
Running...
100%|██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 30000/30000 [7:20:56<00:00,  1.13it/s]
MEMO adapt test error 51.28

rendition level 0
Resuming from results/imagenet_rn50_moex/...
Test: [  0/118] Time 11.405 (11.405)    Acc@1   0.25 (  0.25)
Test: [ 10/118] Time  0.174 ( 1.195)    Acc@1   0.39 (  0.31)
Test: [ 20/118] Time  0.201 ( 0.727)    Acc@1   0.20 (  0.31)
Test: [ 30/118] Time  0.238 ( 0.610)    Acc@1   0.50 (  0.33)
Test: [ 40/118] Time  0.176 ( 0.556)    Acc@1   0.28 (  0.36)
Test: [ 50/118] Time  0.174 ( 0.530)    Acc@1   0.22 (  0.35)
Test: [ 60/118] Time  0.175 ( 0.493)    Acc@1   0.29 (  0.34)
Test: [ 70/118] Time  1.039 ( 0.472)    Acc@1   0.32 (  0.34)
Test: [ 80/118] Time  0.176 ( 0.449)    Acc@1   0.47 (  0.34)
Test: [ 90/118] Time  0.177 ( 0.443)    Acc@1   0.26 (  0.35)
Test: [100/118] Time  0.175 ( 0.420)    Acc@1   0.64 (  0.37)
Test: [110/118] Time  0.180 ( 0.403)    Acc@1   0.27 (  0.36)
 * Acc@1 0.355
Error on corrupted test set 64.48
Resuming from results/imagenet_rn50_moex/...
Running...
██████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 30000/30000 [7:23:11<00:00,  1.13it/s]
MEMO adapt test error 61.87
```

</details>