Here we store the data for the nonlinear diffusion PDE described in Appendix. The other data files are larger than the Github's limit, so we openly distribute them via [OneDrive](https://chula-my.sharepoint.com/:f:/g/personal/pongpisit_t_alumni_chula_ac_th/EtASN5hO5X9AoQPDx9DAaMwBY-rjlieAaA2eVQl4sI_TBQ?e=5JzRmt) (password: nPIML_appendix) instead.

1. Navier-Stokes PDE: `Cylinder_{U, V, W}.npy` are the simulated solutions. `nv_originalv2_noiselv2.h5` contains the noisy polynomial candidate library and the corresponding time derivative vector.
2. 2D Reaction-Diffusion PDE: `reaction_diffusion_2d_big.mat`
3. 3D Reaction-Diffusion PDE: `reaction_diffusion_3d_{128, 64, 32}.mat`. 128, 64 and 32 denote the different numbers of points in the three spatial directions.

-
The specification of the "py3.7" conda environment used *only to* produce the results in the appendix section is given in [env_spec](env_spec/).

The outputs of the following commands are stored.  

1. `conda env export > env_spec/conda_env_nPIML_appendix.yml`
2. `conda list > env_spec/conda_list_nPIML_appendix.txt`
3. `pip list > env_spec/pip_list_nPIML_appendix.txt`
4. `pip freeze --all > env_spec/pip_freeze_nPIML_appendix.txt`