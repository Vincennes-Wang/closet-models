# closet-models

[衣橱](https://github.com/Vincennes-Wang/closet) 应用用的模型文件，通过 GitHub Pages 提供下载（https://vincennes-wang.github.io/closet-models/）。
原因：中国大陆的网页打不开 huggingface.co 和 hf-mirror.com（2026-10-12 实测），GitHub Pages 能打开。

目录结构和 Hugging Face 一样（`<模型>/resolve/main/<文件>`），所以 transformers.js 只要改 `env.remoteHost`。

## Marqo/marqo-fashionSigLIP

- 来源：https://huggingface.co/Marqo/marqo-fashionSigLIP ，版本 `c56244cc94f92419e8369fa71efdaf403b124ce8`
- 许可证：Apache-2.0（见 `LICENSE`），版权归 Marqo。文件未修改。
- 只放应用用到的图像模型（标签文字向量在 closet 仓库里预先算好）。

| 文件 | 大小 | sha256 |
|---|---|---|
| `config.json` | 302 B | `263c127b4cdd236c335fdc4e53933f2764cab2e901ead8d5299fb356967b58c0` |
| `preprocessor_config.json` | 516 B | `6c3b28abcf2e5e59bef07831f580e125100c15aabe23ed06f5565fe620e51dd8` |
| `onnx/vision_model_q4f16.onnx`（WebGPU） | 53.7 MB | `988c55937d35228f860bcc90742940ec3efe8d00054518249f6c82b66e1b4a7c` |
| `onnx/vision_model_int8.onnx`（WASM） | 94.0 MB | `dae6e934667af50590c3d0ca69c7b14edc71f4df1b4f670e5ba6bc623495b691` |

两个 `.onnx` 的 sha256 与 Hugging Face 记录的 LFS sha256 一致。

不放抠图模型 RMBG-1.4：Bria 非商用许可，下载需要填表，许可原文链接打不开，不转发。
