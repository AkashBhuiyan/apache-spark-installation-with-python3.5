# apache-spark-2.3.2-installation-with-python3.5

# java installation:

sudo add-apt-repository ppa:webupd8team/java <br />
sudo apt-get update <br />
sudo apt-get install oracle-java8-installer <br />

to confirm installation: <br />
java -version <br />

# scala installation:

cd Downloads <br />
wget https://downloads.lightbend.com/scala/2.11.12/scala-2.11.12.deb <br />
sudo dpkg -i scala-2.11.12.deb <br />

to confirm installation: <br />
scala -version <br />

# conda installation: <br />
cd /tmp <br />
curl -O https://repo.anaconda.com/archive/Anaconda3-5.3.0-Linux-x86_64.sh <br />
sha256sum Anaconda3-5.3.0-Linux-x86_64.sh <br />
bash Anaconda3-5.3.0-Linux-x86_64.sh <br />
source ~/.bashrc <br />

create environment setup for python 3.5 with conda: <br />
conda create --name apache_spark_py35 python=3.5 <br />
source activate apache_spark_py35 <br />
conda update --all <br />
pip3 install py4j <br />

# finally spark installation: <br />

cd /home/akash <br />
wget http://www-us.apache.org/dist/spark/spark-2.3.2/spark-2.3.2-bin-hadoop2.7.tgz <br />
sudo tar -zxvf spark-2.3.2-bin-hadoop2.7.tgz <br />

export SPARK_HOME='home/akash/spark-2.3.2-bin-hadoop2.7' <br />
export PATH=$SPARK_HOME:$PATH <br />
export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH <br />
export PYSPARK_DRIVER_PYTHON="jupyter" <br />
export PYSPARK_DRIVER_PYTHON_OPTS="notebook" <br />
export PYSPARK_PYTHON=python3 <br />

# For test: <br />
source activate apach_spark_py35 <br />
cd spark-2.3.2-bin-hadoop2.7 <br />
cd python <br />
python <br />
import pyspqrk <br />





