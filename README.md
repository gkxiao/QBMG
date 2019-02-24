# QBMG: Quasi-Biogenic Molecule Generator with Deep Recurrent Network 
## Introduction
This is a PyTorch implementation of the paper: [QBMG: quasi-biogenic molecule generator with deep recurrent neural network](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-019-0328-9)
![Graph abstract](https://github.com/SYSU-RCDD/QBMG/blob/master/image/Graphical%20abstract.png) 
The user can (i) obtain a certain number of unbiased biogenic-like molecules and (ii) obtain a certain number of focused chemotype derivatives with transfer learning.We thank [the previous work by the Olivecrona team](https://github.com/MarcusOlivecrona/REINVENT).The code in this repository is inspired on REINVENT.

## Usage
- sample.py: script that is used to generate a certain number of molecules (both unbiased or certain chemotype biogenic-like molecules) with trained model. 

  **Example:sampling 1000 molecules from unbiased model and focused chemotype model respectively**
``` Python
   %run sample.py ./data/biogenic.ckpt 1000
```
``` Python
   %run sample.py ./data/coumarin.ckpt 1000
```

- transfer_learning.py: script that is used to train focused chemotype biogenic moleucles and obtain focused chemotype derivatives. The user can provide own focused chemotype molecules to generate new derivatives.

  **Example:training a focused chemotype library**
``` Python
   %run transfer_learning.py ./data/coumarin.smi 
```

## Requirments
This package requires:
- Python 3.6
- PyTorch 0.4.0
- RDKit
- tqdm
- jupyter notebook

## Contact
Welcome to contact us.
http://www.rcdd.org.cn/home/

## Added zinc fragment model
ZINC Fragment database was used to train prior model so that it can be used to generate fragment-like molecules.
Welcome to contact me: gkxiao(at)molcalx.com, replace the (at) with @.
More detailed information in Chinese:
http://blog.molcalx.com.cn/2019/02/24/deep-learning-for-fragment-replace.html
![invent new fragment](https://github.com/gkxiao/QBMG/blob/master/image/fragment-example.png) 
