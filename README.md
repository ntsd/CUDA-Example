CUDA-Example



How to set CUDA in Visual Studio 2017
change path from $(VCTargetsPath) to $(VCTargetsPath14)

Example

```
<Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
<ImportGroup Label="ExtensionSettings">
<Import Project="$(VCTargetsPath14)\BuildCustomizations\CUDA 8.0.props" />
</ImportGroup>

<Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
<ImportGroup Label="ExtensionTargets">
<Import Project="$(VCTargetsPath14)\BuildCustomizations\CUDA 8.0.targets" />
</ImportGroup>
```
