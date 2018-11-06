Bootstrap: shub
From: ISU-HPC/augustus


%labels
MAINTAINER ynanyam@iastate.edu

%post

cd /
wget http://topaz.gatech.edu/GeneMark/tmp/GMtool_8oebP/gm_et_linux_64.tar.gz
tar xvf gm_et_linux_64.tar.gz
rm gm_et_linux_64.tar.gz
cd gm_et_linux_64
wget http://topaz.gatech.edu/GeneMark/tmp/GMtool_8oebP/gm_key_64.gz
echo 'export PATH=/gm_et_linux_64/gmes_petap:$PATH' >>$SINGULARITY_ENVIRONMENT
echo 'export LANG=C' >>$SINGULARITY_ENVIRONMENT
cpan App::cpanminus

cpanm YAML File::Spec::Functions Hash::Merge List::Util Logger::Simple Module::Load::Conditional Parallel::ForkManager POSIX Scalar::Util::Numeric File::Which

apt-get install -y ncbi-blast+ bamtools python3-biopython

cd /
wget https://github.com/Gaius-Augustus/BRAKER/archive/v2.1.2.tar.gz

tar xvf v2.1.2.tar.gz
rm v2.1.2.tar.gz
echo 'export PATH=/BRAKER-2.1.2/scripts:$PATH' >>$SINGULARITY_ENVIRONMENT
