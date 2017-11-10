# sfn17
A repository containing our SfN code. 

# Dependencies

## Packages

To use the notebooks included here, please first install the following packages:

```
install.packages(c('ggplot2','latex2exp','igraph','devtools'))
require('devtools')
install_github('neurodata/fmriutils')
```

## Data

The data for the notebooks can be downloaded as follows:

```
sudo mkdir /data/
sudo chmod -R 777 /data

cd /data
wget http://openconnecto.me/mrdata/share/derivatives/dwi_edgelists.tar.gz
wget http://openconnecto.me/mrdata/share/derivatives/fmri_edgelists.tar.gz
wget http://openconnecto.me/mrdata/share/connectome_stats/connectome_stats.zip

mkdir -p /data/connectome_stats /data/dwi/edgelists /data/fmri/ranked/edgelists
mv dwi_edgelists.tar.gz /data/dwi/edgelists
cd /data/dwi/edgelists
tar -xvzf dwi_edgelists.tar.gz
mv /data/fmri_edgelists.tar.gz /data/fmri/ranked/edgelists
cd /data/fmri/ranked/edgelists
tar -xvzf fmri_edgelists.tar.gz
mv /data/connectome_stats.zip /data/connectome_stats.zip
cd /data/connectome_stats
unzip connectome_stats.zip
```
