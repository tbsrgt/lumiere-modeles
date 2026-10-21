# Modèles IA de Lumière

Les modèles ONNX téléchargés par Lumière au premier usage de ses fonctions d'IA locale (tout tourne sur l'ordinateur, la photo n'est envoyée nulle part).

Les fichiers sont dans les [Releases](../../releases).

| Fichier | Origine | Licence |
|---|---|---|
| `realesr-general-x4v3.onnx` | [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) (Xintao Wang), poids `realesr-general-x4v3.pth` convertis en ONNX | BSD-3-Clause, voir `LICENSE-Real-ESRGAN` |
| `realesrgan-x4plus.onnx` | [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) (Xintao Wang), poids `RealESRGAN_x4plus.pth` convertis en ONNX | BSD-3-Clause, voir `LICENSE-Real-ESRGAN` |
| `birefnet-lite.onnx` (release v3) | [BiRefNet](https://github.com/ZhengPeng7/BiRefNet) lite (Zheng Peng et al.), export ONNX de [onnx-community/BiRefNet_lite-ONNX](https://huggingface.co/onnx-community/BiRefNet_lite-ONNX) | MIT, voir `LICENSE-BiRefNet` |
| `codeformer.onnx` (release v4) | [CodeFormer](https://github.com/sczhou/CodeFormer) (Shangchen Zhou et al.), poids `codeformer.pth` v0.1.0 convertis en ONNX | **S-Lab License 1.0 : usage non commercial uniquement**, voir `LICENSE-CodeFormer` |
| `yunet.onnx` (release v4) | [YuNet](https://github.com/opencv/opencv_zoo/tree/main/models/face_detection_yunet) 2023mar (Shiqi Yu), détection des visages | MIT, voir `LICENSE-YuNet` |
| `lama.onnx` (release v2) | [LaMa](https://github.com/advimman/lama) big-lama (Samsung AI), export ONNX de [Carve/LaMa-ONNX](https://huggingface.co/Carve/LaMa-ONNX) (`lama_fp32.onnx`) | Apache-2.0, voir `LICENSE-LaMa` |

Real-ESRGAN : entrée `entree` / sortie `sortie`, RGB 0–1, NCHW, taille libre, agrandissement ×4.

LaMa : entrées `image` (RGB 0–1, zone à effacer mise à 0) et `mask` (0/1), 512 × 512 ; sortie `output` RGB 0–255.

BiRefNet : entrée `input_image` (RGB normalisé ImageNet, 1024 × 1024), sortie `output_image` (logits du masque du sujet, 1024 × 1024).

CodeFormer : entrées `x` (visage aligné 512 × 512, RGB −1..1) et `w` (fidélité 0..1), sortie `y` (−1..1). YuNet : entrée `input` 640 × 640 BGR 0–255.
