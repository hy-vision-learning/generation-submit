# 24-2 시각지능학습 Image Generation

## 1. Clone the repository

```shell
git clone https://github.com/hy-vision-learning/generation-submit
```

## 2. Move to generation-submit

```shell
cd ./generation-submit
```

## 3. Install Required Packages

All required packages can be installed via requirements.txt.
```shell
pip install -r requirements.txt
```

> [!NOTE]
> If an error related to package versions occurs during installation, remove the version information and try again.

## 4. Change the random seed

Open the [change_randomseed.py](./change_randomseed.py) file and change the random seed.

## 5. 평가 데이터 생성

아래 명령어를 실행해서 성능 평가를 위한 데이터를 생성합니다.
```shell
python3 generate_inception_data.py
```

## 	6. Run the code

아래 명령어를 실행해서 학습을 진행합니다.
```shell
python3 main.py  --model BIGGAN --num_epochs 600 --save_every 1000 --test_every 500 --full_test_counter 10 --superclass 1 --dict_size 4 --commitment 10.0 --dict_decay 0.9
```

## 7. Check the Results

save/biggan/날짜 폴더 내부에 생성된 log 파일에서 
