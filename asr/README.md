# Quran speech model (رفيق الحفظ)

`quran-asr-1.onnx` (split into `.part0` and `.part1`; joined they are 174,745,699 bytes,
SHA-256 `9f1e5a60be47de8ea9fde3d8159008e0bf7e7384e791cd318fa10efdcafd6e4a`) is the on-device
speech model the app downloads for «التسميع مع المتابعة».

## Attribution (CC BY 4.0)

This is a modified version of NVIDIA's Arabic FastConformer:

- **Original model:** [`nvidia/stt_ar_fastconformer_hybrid_large_pcd_v1.0`](https://huggingface.co/nvidia/stt_ar_fastconformer_hybrid_large_pcd_v1.0), © NVIDIA Corporation
- **ONNX export of its CTC branch:** [`hamdanfatah19/kotes`](https://huggingface.co/hamdanfatah19/kotes)
- **License:** [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/)

**Changes made:** the weights of the MatMul/Gemm layers were quantised to 8 bits with ONNX Runtime's
dynamic quantisation (`quantize_dynamic`, QInt8) to fit on a phone; nothing else was changed, and the
file was split in two for hosting.

NVIDIA does not endorse this app. Provided as is, without warranties of any kind.
