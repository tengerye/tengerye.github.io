# Server related
1. [Set remote SSH](https://zhuanlan.zhihu.com/p/191627275).
2. [Install NVIDIA driver and CUDA](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/).
3. [Docker install](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository). [Run docker without sudo](https://docs.docker.com/engine/install/linux-postinstall/).


# Visual Studio Code
## Remote connect
1. Install "remote explorer" and "remote ssh" extensions.
2. You can see the "remote explorer" on the left side bar on Visual Studio Code.

## Python extensions
[Code navigation](https://blog.csdn.net/weixin_39947522/article/details/110475013).

## Docker related
Export container to image:
docker commit CONTAINER_ID yetengqi/hpu:version1

Run container:
docker run -it -p 8888:8888 -v /home/tye/projects:/projects --runtime=habana -e HABANA_VISIBLE_DEVICES=all -e OMPI_MCA_btl_vader_single_copy_mechanism=none --cap-add=sys_nice --net=host --ipc=host yetengqi/hpu:version1

Inside docker container:
jupyter lab --allow-root --ip 0.0.0.0