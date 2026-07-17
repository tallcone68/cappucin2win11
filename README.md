<h1 align="center">Catppuccin for Windows 11</h1>

# Instalasi
### NileSoft Shell

1. unduh NileSoft Shell [di sini](https://nilesoft.org/download/shell/1.9.18/setup-x64.msi)
2. jalankan file .msi untuk instalasi hingga selesai
3. download file [theme.nss](nilesoft/theme.nss)
4. copy lalu paste ke "C:\Program Files\Nilesoft Shell\imports" disitu ada banyak file tapi untuk tema atau penampilan fokus ke theme.nss
5. terapkan dengan Ctrl + Right Click agar tema klik kanan diterapkan

_Catatan: setelahnya klik kanan biasa akan langsung menerapkan tema tanpa harus klik Ctrl_



### Windhawk
1. unduh windhawk [di sini](https://ramensoftware.com/downloads/windhawk_setup.exe)
2. jalankan file .exe nya hingga instalasi selesai
3. klik explore lalu cari Custom Window Corner Radius, Windows 11 Notification Center Styler, Windows 11 Start Menu Styler, Windows 11 Taskbar Styler, dan Resource Redirect(opsional). klik details lalu install untuk mengunduh
4. pergi ke [sini](windwahk) copy paste isi file sesuai nama dari mod di windhawk. caranya, klik details di mod tersebut lalu, klik tab advanced fokus ke Mod settings
![](Preview/windhawk.png)
5. jangan lupa klik save agar configurasi berhasil.



### komorebic
1.
 ```powershell
scoop bucket add extras
```
copy paste di powershell


2. lalu install komorebi dan whkd
```powershell
scoop install komorebi whkd
```


3. jika belum install scoop, install dulu. jalankan 2 baris ini di powershell sebagai administrator:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://scoop.sh | Invoke-Expression
```


4. agar komorebi langsung aktif saat komputer menyala jalankan ini di powershell:
```powershell
komorebic enable-autostart --whkd
```


5. config
```powershel
komorebic quickstart
komorebic start --whkd
```
akan muncul file di direktori c:/Users/<nama_user>
unduh file [komorebic.json](komorebic/komorebi.json) dan timpa file komorebic.json di sana
di titik ini fitur snap windows di w11 sebaiknya dimatikan
![](Preview/snap-w11.png)



### masir
1. unduh [installer masir](https://github.com/LGUG2Z/masir/releases/download/v0.1.2/masir-0.1.2-x86_64.msi) (versi 0.1.2) cek ke [sini](https://github.com/LGUG2Z/masir/releases) untuk versi terbaru
2. masir berfungsi untuk mengubah fokus window pakai kursor 
3. restart komorebi dengan masir
```powershell
komorebic stop --whkd
komorebic start --whkd --masir
komorebic enable-autostart --whkd --masir
```



### YASB
1. install dulu [jetbrainsmono propo](https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.zip)
2. ekstrak isi folder tersebut lalu install
![](Preview/nerd-font.png)
3. install yasb via scoop
```powershell
scoop bucket add extras
scoop install extras/yasb
```


4. unduh 3 file [di sini](YASB)
5. copy paste 3 file tersebut ke config folder yasb (C:\Users\<nama user>\.config\yasb), lalu timpa file yang ada di sana
6. tinggal jalankan yasb dan menu bar akan muncul di atas

_Catatan: YASB harus di jalankan manual saat komputer baru dinyalakan_



### cava 
1. unduh file config di [sini](cava)
2. sambil menunggu install cava lewat powershell sebagai administrator

via winget
```powershell
winget install -e --id karlstav.cava
```

atau via scoop
```powershell
scoop install extras/cava 
```



### tacky-border (opsional karena komorebi punya border bawaan di file komorebic.json)
1. install dulu [visual studio code](https://visualstudio.microsoft.com/downloads/) dan rust:
```powershell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

2. klon repo, dan jalankan tacky-border
```powershell
git clone https://github.com/lukeyou05/tacky-borders.git
cd tacky-borders
cargo build --release
cargo run --release
```
3. unduh file [config.yaml](tacky-border/config.yaml)
4. copy paste ke folder config tacky-border

_Catatan: tacky harus dijalankan manual saat komputer baru dinyalakan. maka dari itu, disarankan pakai border yang ada di komorebic_



### terminal
1. buka terminal, buka setting (Ctrl + ,) klik open json file di pojok kiri bawah
2. copas isi file [setting.json](terminal/setting.json)
3. atur $PROFILE ketik ini do powershell:
```poweshell
notepad $PROFILE
```

4. masukkan ini ke dalam file tersebut:
```poweshell
$env:Path += ";$env:ProgramData\starship"
Invoke-Expression (&starship init powershell)

fastfetch
```



## hal lain yang ku install tanpa konfig
1. cmatrix klik di [sini](https://github.com/nxstynate/cmatrix-win/releases/download/cmatrix/cmatrix.exe). untuk versi terbaru klik [di sini](https://github.com/nxstynate/cmatrix-win/releases/download/cmatrix)
2. clock-rs 
```poweshell
cargo install clock-rs
```
4. pipes-rs 
```poweshell
scoop install pipes-rs
```
5. btop 
```poweshell
scoop install btop
```
6. fastfetch / winfetch
```poweshell
scoop install fastfetch
```
7. vs-code [install](https://code.visualstudio.com/)
8. microsoft powertoys
9. starship
```poweshell
winget install starship
```

atau:

```poweshell
scoop install starship

```


### Done
