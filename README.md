Online Robust PCA
=================

Batch and Online Robust PCA (Robust Principal Component Analysis) implementation and examples (Python).

Robust PCA based on Principal Component Pursuit (**RPCA-PCP**) is the most popular RPCA algorithm which decomposes the observed matrix M into a low-rank matrix L and a sparse matrix S by solving Principal Component Pursuit:

> \min ||L||_* + \lambda ||S||_1

> s.t. L + S = M

where ||.||_* is a nuclear norm, ||.||_1 is L1-norm. 

What is inside?
===============
Folder **rpca** contains various batch and online Robust PCA algorithms.

  * pcp.py: Robust PCA based on Principal Component Pursuit (RPCA-PCP). Reference: Candes, Emmanuel J., et al. "Robust principal component analysis." Journal of the ACM (JACM) 58.3 (2011): 11.

  * spca.py: Stable Principal Component Pursuit (Zhou et al., 2009). This implementation uses the Accelerated Proximal Gradient method with a fixed mu_iter. Reference: Zhou, Zihan, et al. "Stable principal component pursuit." Information Theory Proceedings (ISIT), 2010 IEEE International Symposium on. IEEE, 2010. 

  * spca2.py: Stable Principal Component Pursuit (Zhou et al., 2009). This implementation uses the Accelerated Proximal Gradient method with a decreasing mu_iter. Reference: Zhou, Zihan, et al. "Stable principal component pursuit." Information Theory Proceedings (ISIT), 2010 IEEE International Symposium on. IEEE, 2010. 

  * stoc_rpca.py: Online Robust PCA via Stochastic Optimization	(Feng, Xu and Yan, 2013). Reference: Feng, Jiashi, Huan Xu, and Shuicheng Yan. "Online robust pca via stochastic optimization."" Advances in Neural Information Processing Systems. 2013.

  * omwrpca.py: Online Moving Window Robust PCA.

  * omwrpca_cp.py: Online Moving Window Robust PCA with Change Point Detection. A novel online robust principal component analysis algorithm which can track both slowly changing and abruptly changed subspace. The algorithm is also able to automatically discover change points of the underlying low-rank subspace.

Folder **simulation** contains code to reproduce all simulation studies of the paper Xiao, Wei, et al. "Online Robust Principal Component Analysis with Change Point Detection" arXiv (2017).

Folder **example/survillance** contains ipython notebooks to apply the online rpca algorithms for real-world video survillance data. Before running the corresponding ipython notebooks, please first download the video data from <http://perception.i2r.a-star.edu.sg/bk_model/bk_index.html>.

Citation
========
If you use this package in any way, please cite the following publication.
```
@ARTICLE{xiao2017omwrpca,
   author = {{Xiao}, W. and {Huang}, X. and {Silva}, J. and {Emrani}, S. and {Chaudhuri}, A.},
   title = "{Online Robust Principal Component Analysis with Change Point Detection}",
   journal = {ArXiv e-prints},
   archivePrefix = "arXiv",
   eprint = {1702.05698},
   primaryClass = "cs.LG",
   keywords = {Computer Science - Learning, Computer Science - Computer Vision and Pattern Recognition, Statistics - Applications, Statistics - Computation, Statistics - Machine Learning},
   year = 2017,
   month = feb,
   adsurl = {http://adsabs.harvard.edu/abs/2017arXiv170205698X},
   adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```
        


