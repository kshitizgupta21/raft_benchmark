###1. Get RAFT repo
```
git clone https://github.com/rapidsai/raft.git -b branch-24.02
``` 

###3. Launch Mamba docker
```
bash mamba_docker.sh
```

###2. Create conda env rapids_raft
```
bash create_condaenv.sh
```

###3. Activate the environment
```
conda activate rapids_raft
```

###4. Build bench-ann
```
bash build_raft.sh
```

###5. To save container use docker commit
```
docker commit c859cd0fa144 raft22.04
```

###6. To launch container use
```
docker run -it --rm --net=host --gpus=all -v ${PWD}:/workspace -w /workspace raft22.04 bash
```


