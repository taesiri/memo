# Reproducing Results from the paper

## Environment Details

```bash
Python version: Python 3.9.7 | packaged by conda-forge | (default, Sep 29 2021, 19:20:46) 
[GCC 9.4.0] on linux

PyTorch version: 1.13.1+cu117

CUDA version: 11.7
```

## Update `Jan 7, 2022`

Using the [new commit](https://github.com/zhangmarvin/memo/commit/76b37770869e7b3523922b562e0ae001b48d0ad9):

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
    <th class="tg-amwm">ImageNet-A</th>
    <th class="tg-amwm">Run-1</th>
    <th class="tg-amwm">Paper</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-fymr">ResNet-50</td>
    <td class="tg-dvpl">100.0</td>
    <td class="tg-lqy6">100.0</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">99.2</td>
    <td class="tg-lqy6">99.1</td>
  </tr>
  <tr>
    <td class="tg-fymr">DeepAug+AugMix</td>
    <td class="tg-dvpl">96.1</td>
    <td class="tg-lqy6">96.1</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">94.8</td>
    <td class="tg-lqy6">94.8</td>
  </tr>
  <tr>
    <td class="tg-fymr">MoEx+CutMix</td>
    <td class="tg-dvpl">92.0</td>
    <td class="tg-lqy6">91.9</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">89.1</td>
    <td class="tg-lqy6">89.0</td>
  </tr>
</tbody>
</table>



## Results  `ImageNet-R`


<table class="tg">
<thead>
  <tr>
    <th class="tg-amwm">ImageNet-R</th>
    <th class="tg-amwm">Run-1</th>
    <th class="tg-amwm">Paper</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-fymr">ResNet-50</td>
    <td class="tg-dvpl">63.8</td>
    <td class="tg-lqy6">63.9</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">58.7</td>
    <td class="tg-lqy6">58.8</td>
  </tr>
  <tr>
    <td class="tg-fymr">DeepAug+AugMix</td>
    <td class="tg-dvpl">53.2</td>
    <td class="tg-lqy6">53.2</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">49.1</td>
    <td class="tg-lqy6">49.2</td>
  </tr>
  <tr>
    <td class="tg-fymr">MoEx+CutMix</td>
    <td class="tg-dvpl">64.4</td>
    <td class="tg-lqy6">64.5</td>
  </tr>
  <tr>
    <td class="tg-dvpl">+Memo</td>
    <td class="tg-dvpl">59.4</td>
    <td class="tg-lqy6">59.4</td>
  </tr>
</tbody>
</table>

