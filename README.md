# ODH Grandeur

#Pull from github: 
git clone https://github.com/UPHL-BioNGS/Grandeur.githttps://github.com/UPHL-BioNGS/Grandeur.git

#Test data is available but has to be pulled down through fasterq-dump (Part of SRA Toolkit)
#Make sure SRA Toolkit is Downloaded
docker pull ncbi/sra-tools 

#Downloading SRA Toolkit: https://github.com/ncbi/sra-tools/wiki/01.-Downloading-SRA-Toolkit
docker pull ncbi/sra-tools

#Guide on Installing SRA Toolkit: https://github.com/ncbi/sra-tools/wiki/02.-Installing-SRA-Toolkit
#Installing SRA Toolkit
wget --output-document sratoolkit.tar.gz https://ftp-trace.ncbi.nlm.nih.gov/sra/sdk/current/sratoolkit.current-ubuntu64.tar.gz
tar -vxzf sratoolkit.tar.gz
export PATH=$PATH:$PWD/sratoolkit.3.0.0-ubuntu64/bin
which fastq-dump

#Test to see if it works: 
fastq-dump --stdout SRR390728 | head -n 8
