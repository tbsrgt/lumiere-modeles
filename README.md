# Modèles IA de Lumière

Les modèles ONNX téléchargés par Lumière au premier usage de ses fonctions d'IA locale (tout tourne sur l'ordinateur, la photo n'est envoyée nulle part).

Les fichiers sont dans les [Releases](../../releases).

| Fichier | Origine | Licence |
|---|---|---|
| `realesr-general-x4v3.onnx` | [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) (Xintao Wang), poids `realesr-general-x4v3.pth` convertis en ONNX | BSD-3-Clause, voir `LICENSE-Real-ESRGAN` |
| `realesrgan-x4plus.onnx` | [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) (Xintao Wang), poids `RealESRGAN_x4plus.pth` convertis en ONNX | BSD-3-Clause, voir `LICENSE-Real-ESRGAN` |
| `lama.onnx` (release v2) | [LaMa](https://github.com/advimman/lama) big-lama (Samsung AI), export ONNX de [Carve/LaMa-ONNX](https://huggingface.co/Carve/LaMa-ONNX) (`lama_fp32.onnx`) | Apache-2.0, voir `LICENSE-LaMa` |

Real-ESRGAN : entrée `entree` / sortie `sortie`, RGB 0–1, NCHW, taille libre, agrandissement ×4.

LaMa : entrées `image` (RGB 0–1, zone à effacer mise à 0) et `mask` (0/1), 512 × 512 ; sortie `output` RGB 0–255.
