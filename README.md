# Auto-last-text
4. ติดตั้ง Plugin หรือ Shell Prompt เสริม:

ติดตั้ง zsh และใช้ปลั๊กอิน เช่น oh-my-zsh เพื่อเพิ่มฟีเจอร์ auto-suggestion ที่คล้ายกับในภาพ
![Screenshot_2024-11-18-19-30-51-33_84d3000e3f4017145260f7618db1d683](https://github.com/user-attachments/assets/b14f947a-d445-4f91-9cfb-4fbbb86ed4a5)

```shell
pkg install zsh
chsh -s zsh
pkg install git
git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
zsh
```

## หากต้องการ auto-suggestion ให้ติดตั้งปลั๊กอินเพิ่มเติม เช่น:

```
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
echo "source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
source ~/.zshrc
```
หลังจากนี้ Terminal ของคุณจะมีคำแนะนำการเติมคำอัตโนมัติให้โดยตรงในระหว่างพิมพ์คำสั่ง

## ปรับแต่งสีให้เป็นสีเขียว: แก้ไขไฟล์ ~/.zshrc เพื่อกำหนดสีของข้อความคำแนะนำ:
![Screenshot_2024-11-18-19-40-42-92_84d3000e3f4017145260f7618db1d683](https://github.com/user-attachments/assets/4e80b990-1898-480c-9a82-263b9d2dc4ea)


```
echo "ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=green'" >> ~/.zshrc
```

หรือเปิดไฟล์ ~/.zshrc ด้วยโปรแกรมแก้ไข เช่น nano:

```
nano ~/.zshrc
```

แล้วเพิ่มบรรทัดนี้ลงไป:

```
ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=green'
```

3. รีโหลดการตั้งค่า: ใช้คำสั่งนี้เพื่อให้การตั้งค่ามีผลทันที:

```
source ~/.zshrc
```
## ຄຳສັ່ງ PROMPT 
## ສຳຫລັບ nano ~/.zshrc


![Screenshot_2024-11-25-18-39-54-02_84d3000e3f4017145260f7618db1d683](https://github.com/user-attachments/assets/d91d376c-1581-417b-ad52-da9059c60273)

```
PROMPT=$'%F{green}┌─%F{green}SWITCH\n%F{red}Credit %F{green}By Xmas──[%F{yellow}SERVER%~%F{green}]\n%F{green}└─> %F{yellow}'
```
## อธิบายโค้ด:

%F{color}: ใช้สำหรับตั้งค่าข้อความเป็นสีที่ต้องการ

green = สีเขียว

yellow = สีเหลือง


%~: แสดงชื่อไดเรกทอรีปัจจุบันแบบย่อ

%n: ชื่อผู้ใช้

%m: ชื่อเครื่องคอมพิวเตอร์ (hostname)

%~: แสดงที่อยู่ของไดเรกทอรีปัจจุบัน

$: แสดงสัญลักษณ์ prompt (ตามด้วยเครื่องหมาย $ สำหรับผู้ใช้ปกติ หรือ # สำหรับผู้ใช้ root)

%f: รีเซ็ตสี

$'\n': เพิ่มบรรทัดใหม่ (newline)

%F{default}: รีเซ็ตสี (ไม่ต้องระบุในนี้ เพราะสีจะรีเซ็ตเองหลัง prompt จบ)

![Screenshot_2024-11-25-18-54-13-23_84d3000e3f4017145260f7618db1d683](https://github.com/user-attachments/assets/c061989b-7a03-4653-a573-0af18eb4669d)
```
echo -e "\033[0;31m\nHEY\033[0;32m~\033[0;31mFU>
echo -e "\033[1;4;34mXMASH-T\033[0;32m SCRIPT\0>
```

## HOME > nano ~/.zshrc
![Screenshot_2024-11-26-12-26-39-88_84d3000e3f4017145260f7618db1d683](https://github.com/user-attachments/assets/0157d858-0d43-40c9-b780-7750cccb0cae)

```
pkg install figlet lolcat
```
```
figlet "SWICTH" | lolcat
```
