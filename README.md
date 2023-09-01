# About Image Generative AI

<br>

### Latent Diffusion Model이란
- Diffusion Model
  - Diffusion(확산)
    - 비유: 이것은 물컵에 잉크를 한방울 떨어뜨리는 것과 비슷합니다. 잉크가 물속에서 "확산(Diffusion)"하게 되고, 몇분 지나면 물속에 완전히 퍼져버려서 처음에 잉크가 어디에 떨어졌는지 전혀 알 수 없게 되어 버립니다.
   - Reverse Diffusion(역방향 확산)
     - Diffusion Model에서의 이미지 생성 방식
   - Noise predictor(잡음 예측기)
     - U-Net: 사전 학습된 신경망 모델
- Latent Diffusion Model
  - Latent Space(잠재 공간)
    - 학습 및 결과 생성을 빠르고 효율적으로 하기 위해 압축된 공간에서 연산을 시행
  - VAE(Variational AutoEncoder, 가변 자동 인코더)
    - 생성형 모델 중 하나이며 인코더와 디코더로 이루어져 있음
    - 잠재 공간(Latent Space) 생성
    - 이 잠재 공간으로부터 만들어진 결과를 디코딩하여 결과물 생성
- CLIP Model
  - Contrastive Language-Image Pre-training model
  - OpenAI에서 개발
  - ViT(Vision Transformer)와 Transformer 언어 모델(Transformer-based language model)을 결합하여 이미지와 텍스트를 모두 처리할 수 있게 만들어놓은 모델\
  - 사용자가 입력한 프롬프트를 UNet이 이해하고 처리할 수 있는 형식으로 인코딩
- Stable Diffusion 모델의 이미지 생성 방식 요약

<br>

### Parameters
- Prompt
  - 참고
    - https://stable-diffusion-art.com/prompt-guide/#Keyword_blending
    - https://openart.ai/promptbook
- Sampling steps
  - Diffusion model에서 노이즈 제거 과정을 반복하는 횟수
  - 일반적으로 20~25 값 사용
  - 참고용 예시: https://github.com/easydiffusion/easydiffusion/wiki/How-to-Use
- Seed
  - 잠재 공간에서 초기 랜덤 텐서를 생성하는 데 사용되는 값
  - 모든 파라미터들과 seed 값을 고정하면 항상 동일한 이미지가 만들어짐
  - 랜덤값(-1)
- Guidance Scale(Prompt Guidance)
  - 이미지 생성 프로세스가 텍스트 프롬프트를 따르는 정도를 제어하는 파라미터
  - 값이 커질수록 프롬프트와 가까운 이미지가 생성되지만 품질이 저하됨
  - 일반적으로 7~12 값이 권장됨
- Sampler(Sampling method)
  - 노이즈 제거 과정 반복 전의 알고리즘을 결정하는 역할
  - 참고용 예시: https://github.com/easydiffusion/easydiffusion/wiki/How-to-Use
 
<br>
<br>
