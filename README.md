# CPP-Fundamentals-and-Beyond



CPP-Fundamentals-and-Beyond. Repo for learning CPP-Fundamentals

## Installation



Install using msys2.


1. Open the Windows Powershell with administration user.
2. Run the install script from [Chocolatey](https://chocolatey.org/install).
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
3. Run 
```powershell
choco install -y msys2
```
4. Close Powershell and open the directory `C:\tools\msys64\etc\pacman.d`
5. There are three mirror files in it:
   + mirrorlist.mingw32
   + mirrorlist.mingw64
   + mirrorlist.msys
   
   Open and delete every line of them except the line with `https://mirrors.tuna.tsinghua.edu.cn`
6. Open msys2 by `C:\tools\msys64\msys2.exe`
7. Refresh the pacman database
```bash
pacman -Sy
```
8. Install the mingw toolchain and some other utils in msys2
```bash
pacman -S mingw-w64-x86_64-toolchain libraries development compression VCS sys-utils net-utils msys2-devel mingw-w64-x86_64-cmake
```

You may check https://www.jianshu.com/p/c740b71e7775 for reference.


## Usage

```c++
// Your First C++ Program

#include <iostream>

int main() {
    std::cout << "Free_Plastine!";
    return 0;
}

```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
