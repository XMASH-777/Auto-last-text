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

