```sh
winget install Microsoft.VisualStudio.2022.BuildTools --override "--add Microsoft.VisualStudio.Component.VC.Tools.x86.x64 --passive" --source winget
```

```sh
winget install Microsoft.VisualStudio.2022.BuildTools --override "--add Microsoft.VisualStudio.Workload.VCTools --add Microsoft.VisualStudio.Component.Windows10SDK --includeRecommended --passive" --source winget
```

```sh
winget install "Windows 10 SDK" --source winget
```

```sh
Get-ChildItem -Path "C:\Users\wi\AppData\Local\loonghao\msvc-kit\data\VC\Tools\MSVC\14.44.35207\bin\Hostx64\x64" -Recurse -Filter "cl.exe" -ErrorAction SilentlyContinue | Select-Object FullName
```


```sh
$clPath = "C:/Users/wi/AppData/Local/loonghao/msvc-kit/data/VC/Tools/MSVC/14.44.35207/bin/Hostx64/x64/cl.exe";
```

```sh
cmake . -G "Visual Studio 17 2022" -A x64 `
    -DCMAKE_C_COMPILER="C:/Users/wi/AppData/Local/loonghao/msvc-kit/data/VC/Tools/MSVC/14.44.35207/bin/Hostx64/x64/cl.exe" `
    -DCMAKE_CXX_COMPILER="C:/Users/wi/AppData/Local/loonghao/msvc-kit/data/VC/Tools/MSVC/14.44.35207/bin/Hostx64/x64/cl.exe" `
    -B build
```

```sh
Remove-Item -Recurse -Force build -ErrorAction SilentlyContinue
```

```sh
cmake -G "Visual Studio 17 2022" -A x64 -B build
```

```sh
 cmake . -B build
```

```sh
cmake --build build/
```

```sh
./build/Application
```
