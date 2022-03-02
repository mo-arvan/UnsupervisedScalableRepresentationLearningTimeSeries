```bash
docker build -t repo-timeseries -f docker/dockerfile .

docker run --rm  -v /home/ar-gpu-server/workspace/tex-setup/workspace/reproducibility/UnsupervisedScalableRepresentationLearningTimeSeries:/workspace -it repo-timeseries bash

# inside the container

pip insall -r reproducibility/requirements.txt

python3 ucr.py --dataset Mallat --path reproducibility/dataset/UCRArchive_2018 --save_path output --hyper default_hyperparameters.json
```

