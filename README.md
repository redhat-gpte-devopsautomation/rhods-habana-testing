# rhods-habana-hpu-testing
<p>This is a repository providing sample code to test and verify that HPU's are available for your environment and also to run a small tensor based / CUDA based python program on GPUs.</p>
<p>Once you clone this repo on jypyterhub notebook after starting it on RHODS's environment using habana based image, run the notebook `quickstart_tutorial.ipynb` provided in this repo to test and verify HPU's.</p>

<p>If RHODS version is < 1.34, you need to manually add HPU resource to the jupyterhub notebook instance.</p>  
<p>Follow this document if you are using RHODS < 1.33 to set habana hpu's in the notebook instance. <a href="https://docs.google.com/document/d/1v64_nI5zSiFM4PtinXhbfmow2-fJ2guLf-2AbL-lnNM/edit?usp=sharing" target="_blank">Habana Jupyterhub Notebook Instance resource setting for Habana GPUS - For RHODS 1.33 and less </a></p>

<p> Once the instance is saved and reloaded, you can restart your jupyterhub notebook on RHODS dashboard and that should give you access to HPU's when you run your test notebook. Note that this procedure will be obsolete with the release of RHODS 1.34 onwards </p>
