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
