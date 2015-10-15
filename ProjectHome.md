# GPUDWT: Discrete Wavelet Transform accelerated on GPU #

<img src='http://chart.apis.google.com/chart?chs=150x150&cht=qr&chl=GPUDWT%3A+Discrete+Wavelet+Transform+accelerated+on+GPU%0Ahttp%3A%2F%2Fgpudwt.googlecode.com%0Ahttp%3A%2F%2Fwww.sitola.cz&nonsense=something_that_ends_with.png' alt='' width='150' align='right' height='150' />

Discrete Wavelet Transform (DWT) is a broadly used digital signal processing technique with application in diverse areas. GPUDWT library implements forward and revers DWT 9/7 and 5/3 transforms and supports CUDA platform (version 3.2 and newer) and NVIDIA GPUs.


## Performance results ##
On average a HD-sized (1920x1080) image can be transformed within **0.199ms**
using NVIDIA GeForce GTX 580 GPU.

**Results for single color HD (1920x1080) 8bit image:**
| **GPU** | **Transformation type** | **Avg. time (µs)** (1 level / 3 levels) |
|:--------|:------------------------|:----------------------------------------|
| GeForce GTX 580 | Forward DWT 9/7         | 199/351                                 |
| GeForce GTX 580 | Reverse DWT 9/7         | 278/453                                 |
| GeForce GTX 580 | Forward DWT 5/3         | 173/277                                 |
| GeForce GTX 580 | Reverse DWT 5/3         | 190/315                                 |
| GeForce 8600 GT | Forward DWT 9/7         | 5113/7790                               |
| GeForce 8600 GT | Reverse DWT 9/7         | 6439/9310                               |
| GeForce 8600 GT | Forward DWT 5/3         | 3877/5773                               |
| GeForce 8600 GT | Reverse DWT 5/3         | 4281/6301                               |
The times listed are in microseconds (μs) for one-level and
three-levels transformations.

## Installation / Compilation ##

  1. Download source from http://code.google.com/p/gpudwt/downloads/list
  1. Unpack
```
$ tar xfvz gpudwt-XXX.tar.gz
```
  1. Change current directory
```
$ cd gpudwt-XXX
```
  1. Edit 'Makefile' so that 'CUDA\_INSTALL\_PATH' points to CUDA toolkit directory
  1. Run 'make'
```
$ make
```
  1. To get help run
```
$ ./gpudwt --help
```

## References ##
Early gpudwt design was described in paper _GPU-Based DWT Acceleration for JPEG2000_ (http://www.sitola.cz/papers/858064.pdf).

Bibtex entry:
```
@inproceedings{858064,
   author = {Matela, Jiří},
   title = {{GPU-Based DWT Acceleration for JPEG2000}},
   booktitle = {MEMICS 2009 Proceedings},
   year = {2009},
   pages = {136-143},
   address = {Brno},
   isbn = {978-80-87342-04-6}
}
```

Note, we have not described the current design in any paper yet.


## Acknowledgments ##
This project has been supported by a research intent _Optical Network of National
Research and Its New Applications (MSM 6383917201)_ (http://www.cesnet.cz) and _Parallel
and Distributed Systems (MSM 0021622419)_.

<p align='center'>
<a href='http://www.sitola.cz/'>
<img src='http://www.sitola.cz/wordpress/wp-content/themes/sitola/images/sitola_logo_en.gif' alt='www.sitola.cz' border='0' />
</a>
</p>
