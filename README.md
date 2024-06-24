### Installation
1. Clone the repository:
```bash
git clone https://github.com/OrestisVaggelis/FaceAgingCycleGAN.git
cd FaceAgingCycleGAN
```
### Training
1. Training the Base CycleGAN Model

To train the base CycleGAN model, execute the following command:
```bash
python base_cyclegan/train_cyclegan.py
```

2. Training the Self-Attention CycleGAN Model

To train the self-attention CycleGAN model, run the following command:
```bash
python attention_cyclegan/train_attn_cyclegan.py
```

### Inference

After training, you can perform inference using the trained models. Specify the model type (base or attention), the generator transformation (o for old to young, y for young to old), the path to the input image, and the path where the generated image will be saved.

Example for the base model:

```bash
python inference.py --model base --gen o --input /path/to/input_image.jpg --output /path/to/output_image.jpg
```

Example for the base model:
```bash
python inference.py --model attention --gen y --input /path/to/input_image.jpg --output /path/to/output_image.jpg
```
