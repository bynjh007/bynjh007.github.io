## This is the manual how I uploaded the sequencing data to ENA server

Problem: the default mode of ltfp (installed in conda environment) doesn't work from the institute server.  

Solution: the mode of FTP should be changed (passive mode)

```
# access to ENA server
lftp webin2.ebi.ac.uk -u Webin-49379

# change the mode
set ftp:passive-mode true
set ftp:ssl-allow off

# now you can upload the files to ENA
ls # check the files in your home in ENA
mput /path/files
```

