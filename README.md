CUDA-Example



How to set CUDA VS15 in Visual Studio 2017

Move all file 

from
C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\extras\visual_studio_integration\MSBuildExtensions

to
C:\Program Files (x86)\MSBuild\Microsoft.Cpp\v4.0\v140\BuildCustomizations (for VCTargetsPath14)

C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\IDE\VC\VCTargets\BuildCustomizations\ (for VCTargetsPath)


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
ref: https://www.olegtarasov.me/how-to-build-cuda-toolkit-projects-in-visual-studio-2017/