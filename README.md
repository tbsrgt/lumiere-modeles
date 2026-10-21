# Modèles IA de Lumière

Les modèles ONNX téléchargés par Lumière au premier usage de ses fonctions d'IA locale (tout tourne sur l'ordinateur, la photo n'est envoyée nulle part).

Les fichiers sont dans les [Releases](../../releases).

| Fichier | Origine | Licence |
|---|---|---|
| `realesr-general-x4v3.onnx` | [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) (Xintao Wang), poids `realesr-general-x4v3.pth` convertis en ONNX | BSD-3-Clause, voir `LICENSE-Real-ESRGAN` |
| `realesrgan-x4plus.onnx` | [Real-ESRGAN](https://github.com/xinntao/Real-ESRGAN) (Xintao Wang), poids `RealESRGAN_x4plus.pth` convertis en ONNX | BSD-3-Clause, voir `LICENSE-Real-ESRGAN` |

Entrée `entree` / sortie `sortie`, RGB 0–1, NCHW, taille libre, agrandissement ×4.
