# rhods-habana-hpu-testing
<p>This is a repository providing sample code to test and verify that HPU's are available for your environment and also to run a small tensor based / CUDA based python program on GPUs.</p>
<p>Once you clone this repo on jypyterhub notebook after starting it on RHODS's environment using habana based image, run the notebook `quickstart_tutorial.ipynb` provided in this repo to test and verify HPU's.</p>

<p>If RHODS version is < 1.34, you need to manually add HPU resource to the jupyterhub notebook instance.</p>
<p>Once you start the jupyterhub notebook (habana) from RHODS dashboard go and update the resource for this instance from OCP UI / API Explorer.</p>
<p>Search for notebook in API Explorer (1st one will be with v1 api, select that). This will lead you to jypyterhub notebook instance (you need to select instance to get to the habana jupyerhub notebook instance). There will be two containers, select the container with more resources and add habana gpu's as shown below and save the instance.</p>
<yaml>
spec:
  template:
   spec:
:
:
     containers:
     - resources:
       limits:
         cpu: '2'
         habana.ai/gaudi: '1' # Add this line
         memory: 8Gi
       requests:
         cpu: '1'
         habana.ai/gaudi: '1' # Add this line
         memory: 8Gi
</yaml>

<p> Once the instance is saved and reloaded, you can restart your jupyterhub notebook on RHODS dashboard and that should give you access to HPU's when you run your test notebook. Note that this procedure will be obsolete with the release of RHODS 1.34 onwards </p>
