Manual for downloading HMF data. 

Once you obtain the permission to requested HMF data, your account can access the data through GCP.  
The detail manual can be found in [HMF github](https://hartwigmedical.github.io/documentation/accessing-hartwig-data-through-gcp.html).  
In here, very essential steps are described.  

```
# activate conda environment 
conda activate gcloud

# login with your account
gcloud auth login # this will give you the link where you can get the verification code.

# check the files in the given hmf project
gsutil -u hmf-download ls gs://hmf-dr-205/ # 'hmf-download' is the project name where your account is registered (by institutue)

# check the file sizes
gsutil -u hmf-download du -h gs://hmf-dr-205/

# download the metadata, somatic data, and manifest (this is for RNA-seq)
gsutil -u hmf-download cp gs://hmf-dr-205/* /DATA/path/
```

