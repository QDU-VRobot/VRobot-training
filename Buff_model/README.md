openvino读取该模型示例：

```cpp
std::string model_path = "../Buff_model/buff_quantized.xml";
std::shared_ptr<ov::Model> model = core.read_model(model_path);
```

要使用onnx runtime或tensorRT读取该模型，需要先使用openvino提供的cli工具将其转换为onnx格式：

```bash
ovc buff_quantized.xml --output_model buff_quantized.onnx
```

