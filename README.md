# nPIML
---------- Noise-aware physics-informed machine learning (nPIML) ----------

Here, we provide the data that support the findings of the paper "Noise-aware Physics-informed Machine Learning for Robust PDE Discovery".

## Citation
DOI: [https://doi.org/10.1088/2632-2153/acb1f0](https://doi.org/10.1088/2632-2153/acb1f0)  
Pongpisit Thanasutives *et al* 2023 *Mach. Learn.: Sci. Technol.* **4** 015009

Bibtex:  

```
@article{Thanasutives_2023,
	doi = {10.1088/2632-2153/acb1f0},
	url = {https://dx.doi.org/10.1088/2632-2153/acb1f0},
	year = {2023},
	month = {feb},
	publisher = {IOP Publishing},
	volume = {4},
	number = {1},
	pages = {015009},
	author = {Pongpisit Thanasutives and Takashi Morita and Masayuki Numao and Ken-ichi Fukui},
	title = {Noise-aware physics-informed machine learning for robust PDE discovery},
	journal = {Machine Learning: Science and Technology}
}
```

## Open Research Codebase
Please access [OneDrive](https://chula-my.sharepoint.com/:f:/g/personal/pongpisit_t_alumni_chula_ac_th/EqLojgZtNzNJoGZIcJLqTjkBv4VYXoUueFYy8KzGkwzlpA?e=IXAmKX) (password: nPIML) or [GoogleDrive](https://drive.google.com/drive/folders/1hlsO6BuGa4lL1lruBDT-Z6jXWxuFLCZG?usp=share_link). Then you can extract the zip file containing the code you are looking for. The extracted directories are supposed to be at `~/Desktop/`. The related primary directories in `research.zip` include but are not limited to `pysindy`, `parametric-discovery`, `l0bnb_algos`, `abess`, `WSINDy_PDE_JCP`, `SciencePlots` and `PDE-FIND*`. Note that all the data are included already in this codebase.

**Concerning the main text** >>> nPIML framework consists of the three main steps.  
[Step 1]  
- KdV: `ls Multi-task-Physics-informed-neural-networks/inverse_small_KdV/Hyperparameter\ study-approx_l0-reproduced-for-pub*.ipynb`  
- KS: `ls kuramoto-sivashinsky-solver/ks_selector*.py`  
- QHO: `ls kuramoto-sivashinsky-solver/qho.py`  
- NLS: `ls kuramoto-sivashinsky-solver/nls.py`

[Step 2] Mostly in `Multi-task-Physics-informed-neural-networks/`  
- KdV: `ls inverse_small_KdV/Find\ lambda_str*.ipynb`  
- KS: `ls inverse_small_KS2/Find\ lambda_str*.ipynb`  
- QHO: `ls inverse_qho/Find\ lambda_str*ipynb`  
- NLS: `ls inverse_NLS/Find\ lambda_str*.ipynb`

Visit [https://github.com/MathBioCU/WSINDy_PDE](https://github.com/MathBioCU/WSINDy_PDE/) or try running `research/WSINDy_PDE_JCP/wsindy_pde_script_nPIML.m` (MATLAB required) to enable the extension to the convolutional weak formulation (CWF).

[Step 3] Mostly in `kuramoto-sivashinsky-solver/`  
- KdV (a recommended demo): `ls kdv_pinn_2000_pub.py kdv_pinn_2000_pub_20220517.py`  
- KS: `ls deephpm_KS_chaotic_learned_coeffs_*_new.py deephpm_KS_chaotic_learned_coeffs_more_noise.py` 
- QHO: `ls qho_pinn_learned_coeffs_20220613.py`  
- NLS: `nls_pinn_learned_coeffs_20220614.py`

Code regarding all the three steps of Burgers' PDE example resides in `Multi-task-Physics-informed-neural-networks/inverse_burgers/`.  
Step 1: `ls abess-approx_l0-gammaSwish-clean-DEMO-kappa-20220429\ \(pub\).ipynb abess-approx_l0-gammaSwish-clean-DEMO-noise-tolerence*.ipynb`  
Step 2: `ls Find\ lambda_str*.ipynb`  
Step 3: `ls Final\ PINN-wiener-V2-less-samples-20220627-newpub*.ipynb Final\ PINN-Visualize\ noise\ \(freezed\ success\)-pub-reproduced20221204.ipynb`. The last notebook is for the denoising visualization. You may start exploring the notebooks for Burgers' PDE discovery by installing `torch==1.11.0`.

**Concerning the appendix section** >>> Code for the appendix section is all in `research/PDE-FIND/` (a clone of [the PDE-FIND repository](https://github.com/snagcliffs/PDE-FIND)).  

1. Nonlinear Diffusion: `ls Nonlinear-Diffusion-visual-nPIML.ipynb`
2. Navier Stokes: `ls Navier-Stokes\ with\ noise\ original\ data*.ipynb`
3. 2D Reaction Diffusion: `ls Reaction-Diffusion-2D-big-nPIML-pub*.ipynb`
4. 3D Reaction Diffusion: `ls Reaction-Diffusion-3D-nPIML.ipynb`

Please install `research/l0bnb_algos/v2/l0bnb` and `research/abess/python` for running the best-subset regression solvers. The notebooks from 1. to 4. import `best_subset.py` (in `research/parametric-discovery/`), which has helper fuctions (e.g., backward_refinement) written for utilization with the best-subset solvers. To use the weak formulation (WF) algorithm, install `research/pysindy`. Since these repositories are open sources, you may update them by `git pull`.  
Specification of the conda environment (namely "py3.7") used *only for* producing the results in the paper's appendix section is given in [env_spec](data/appendix/env_spec/).  
Please be aware that an act of using external libraries is under their licenses provided in the associated directories.

## Notes
Any dubiousness, questions or requests may be forwarded to the corresponding author.  
Feel free to create an issue on this repository if you have trouble downloading the source codes.