https://roadmap.sh/projects/task-tracker

# task-cli

Таны даалгаврыг удирдах хялбар CLI хэрэгсэл.

## Суурилуулалтын заавар

`task-cli` хэрэгслийг өөрийн машин дээр суулгаж, ажиллуулахын тулд дараах алхмуудыг дагаарай.

### 1. Скриптийг татаж авах
`task-cli.py` скриптыг татаж аваад, жишээлбэл `/c/Users/bazar/bin/` гэх фолдерт байршуулна уу.

### 2. Python суулгагдсан эсэхийг шалгах
Python 3 суулгагдсан эсэхийг шалгаарай. Python суулгасан эсэхээ шалгахын тулд дараах командыг ажиллуулна уу:

```bash
python --version
```

Хэрэв Python суулгагдаагүй бол [python.org](https://www.python.org/downloads/) сайт руу орж, татаж суулгаж болно.

### 3. Python-ийг PATH орчинд нэмэх (Хэрэв хэрэгтэй бол)
Хэрэв Python таны системийн PATH орчинд нэмэгдээгүй бол дараах алхмуудыг дагаж нэмнэ үү:

1. Python хаана суулгагдсан байгааг олно уу, ихэвчлэн дараах байршилд байх болно:
   ```
   C:\Users\<таны_нэр>\AppData\Local\Programs\Python\Python3x\
   ```
2. Python-ийн гүйцэтгэх зам болон `Scripts` фолдерийг системийн PATH орчинд нэмнэ үү.

Жишээ нь, дараах замуудыг PATH орчинд нэмнэ:
```
C:\Users\<таны_нэр>\AppData\Local\Programs\Python\Python312\
C:\Users\<таны_нэр>\AppData\Local\Programs\Python\Python312\Scripts\
```

Windows дээр PATH орчныг нэмэхийн тулд:

1. Windows-ийн хайлтын хэсэгт **Environment Variables** гэж бичиж хайна уу.
2. **Edit the system environment variables** дээр дарна уу.
3. **System Properties** цонхноос **Environment Variables** дээр дарна уу.
4. **System variables** хэсгээс **Path** гэсэн өөрчлөлтийг сонгоод **Edit** дээр дарна уу.
5. Python замуудыг нэмээд, **OK** дарна уу.

### 4. Скриптэд гүйцэтгэх эрх өгөх (Линукс/Мак орчинд л хэрэгтэй)
Линукс эсвэл Мак орчинд ажиллаж байгаа бол скриптэд гүйцэтгэх эрх өгөх шаардлагатай. Дараах командыг терминалд ажиллуулна уу:

```bash
chmod +x /c/Users/bazar/bin/task-cli
```

### 5. Shebang мөрийг засах (Хэрэв Windows дээр ажиллахгүй бол)
Windows хэрэглэгчдэд **task-cli** скрипт нь стандарт shebang мөртэй ажиллахгүй байж магадгүй. Скриптээ нээж, эхний мөрийг Python-ийг зөв зааж өгөхөөр засна уу.

Python гүйцэтгэх замыг олж, shebang мөрийг дараах байдлаар шинэчилнэ үү:

```python
#!C:/Users/bazar/AppData/Local/Programs/Python/Python312/python.exe
```

Энд **Python312** нь таны Python хувилбар бөгөөд, та өөрийн хувилбарын дагуу энэ замыг тохируулна уу.

### 6. Скриптыг ажиллуулах
Одоо та скриптийг дараах командыг ашиглан ажиллуулж болно:

```bash
task-cli --help
```

Хэрэв та **Windows** хэрэглэгч бол `task-cli` шууд ажиллахгүй бол **Python** ашиглан дараах байдлаар ажиллуулна уу:

```bash
python /c/Users/bazar/bin/task-cli --help
```

### 7. Асуудал шийдвэрлэх
- **Permission Denied**: Хэрэв та зөвшөөрлийн алдаа авах бол **chmod +x** командыг ашиглан скриптэд гүйцэтгэх эрх өгөөрэй (Линукс/Мак).
- **Python Олдсонгүй**: Хэрэв Python олоогүй бол, Python суулгагдсан эсэхийг шалгаж, PATH орчинд зөв нэмэгдсэн эсэхийг шалгана уу.
- **Bad Interpreter Алдаа**: Windows дээр хэрэв shebang мөр алдаа өгвөл, скриптэд Python-ийг зөв зааж өгөөрэй.


