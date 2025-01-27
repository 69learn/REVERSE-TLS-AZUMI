
نام پروژه : ریورس تانل WS + WSS[TLS]

<div align="right">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/project-management.png" alt="Video Title" width="100">
  </a>
</div>
  </details>
</div>



-----------------------
**امکانات**
<div align="right">
    <img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/ability.png" alt="Video Title" width="100">
  </a>
</div>
  </details>
</div>



- پشتیبانی از TCP و UDP
- قابلیت تانل بر روی چندین پورت
- امکان استفاده از ایپی 4 و 6
- ریست تایمر انتخابی توسط شما و ویرایش آن (دقیقه یا ساعت)
- امکان استفاده از ساب دامین در ریورس تانل ( باید برایش cert گرفته شود)
- امکان استفاده از چند سرور خارج و یک سرور ایران
- امکان حذف تمامی تانل ها و سرویس ها
 ---------------
- **دستور kill به ریست تایمر اضافه شد. اگر مشکل قطعی داشتید از طریق گزینه edit menu و minutes تایم خود را از ساعت به دقیقه تغییر دهید.**
- **دستور bin bash برای سرور های ایرانی که مشکل اجرا نشدن دستور cron را داشتند، اضافه شد. برای کانفیگ دوباره، نخست uninstall کنید که دستورات cron پیشین پاک شود.**
- **این تانل منابع زیادی میخواهد پس دقت نمایید**
 ------------------------------------------------------
 

 <div align="right">
  <details>
    <summary><strong>توضیحات</strong></summary>
  
------------------------------------ 

- **اگر سرعتتون پایین بود، لطفا هم بر روی سرور ایران و خارج optimizer نصب کنید.**
- اگر در generate کردن key ها مشکل داشتید، حتما اطمینان پیدا کنید که openssl نصب شده باشه. sudo apt-get install pkg-config libssl-dev
- حتما در سرور تست، نخست تانل را ازمایش کنید و سپس اقدام به استفاده از آن بکنید.
- تمامی تست های من با سرورهای کاملا فیلتر شده بوده است.
- در این اسکریپت شما یا با WS، ریورس تانل را برقرار میکنید یا با TLS
- **حدودا پنج ثانیه طول میکشد که ارتباط شما با تانل برقرار شود مخصوصا در کلاینت وایرگارد** (در کلاینت وایرگارد، حدودا 5 ثانیه طول میکشد تا ارتباط شما برای بار اول برقرار شود)
- از TCP و UDP پشتیبانی میکند.
- ریست تایمر برای سرویس های خود را بر اساس نیاز خودتان تعیین کنید.
- در این تانل میتوانید چندین سرور خارج را به یک سرور ایران وصل کنید. اگر از این ریورس تانل راضی بودید، میشود تعداد سرور خارج و ایران را افزایش داد.
- حتما ریست تایمر سرور خارج و ایران یکسان باشد.
- حتما در صورت مشکل دانلود، dns های خود را تغییر دهید.
- پنل شما در خارج باید نصب شده باشد
- اگر به هر دلیلی پیش نیاز ها برای شما نصب نشد و خطا گرفتید، دوباره امتحان بفرمایید.
- اگر به هر دلیلی نتوانستید برای ساب دامین خود cert بگیرید به صورت دستی با acme اینکار را انجام دهید و سپس قسمت cert در اسکریپت را skip کنید.
- اگر اختلالی در تانل داشتید همیشه وارد مسیر روبرو شوید cd /etc/systemd/system و با دستور ls ، سرویس های خارج و ایران را بیابید و با دستور systemctl status servicename و یا journalctl -u servicename.service ، دلیل اختلال تانل را بیابید

  </details>
</div>
  
------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/youtube.png" width="40" alt="Image"> ویدیوهای آموزشی</strong></summary>

- ویدیوی آموزشی توسط 69

<div align="right">
  <a href="https://www.youtube.com/watch?v=AjNrYOpNaQE">
    <img src="https://img.youtube.com/vi/AjNrYOpNaQE/0.jpg" alt="Video Title" width="300">
  </a>
</div>
<div align="right">
  <a href="https://www.youtube.com/watch?v=Avi8ErLPJJE">
    <img src="https://img.youtube.com/vi/Avi8ErLPJJE/0.jpg" alt="Video Title" width="300">
  </a>
</div>
  </details>
</div>


------------------------

 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/right.png" width="40" alt="Image"> اموزش نصب go مورد نیاز برای اجرای اسکریپت</strong></summary>
  
------------------------------------ 

- شما میتوانید از طریق اسکریپت [Here](https://github.com/Azumi67/Reverse_tls/tree/main#%D8%A7%D8%B3%DA%A9%D8%B1%DB%8C%D9%BE%D8%AA-%D9%85%D9%86) ، این پیش نیاز را نصب کنید یا به صورت دستی نصب نمایید.
- حتما در صورت مشکل دانلود، dns های خود را تغییر دهید.
- پس از نصب پیش نیاز ، اجرای اسکریپت go برای بار اول، ممکن است تا 10 ثانیه طول بکشد اما بعد از آن سریع اجرا میشود.
```
sudo apt update
arm64 : wget https://go.dev/dl/go1.21.5.linux-arm64.tar.gz
arm64 : sudo tar -C /usr/local -xzf go1.21.5.linux-arm64.tar.gz

amd64 : wget https://go.dev/dl/go1.21.5.linux-amd64.tar.gz
amd64 : sudo tar -C /usr/local -xzf go1.21.5.linux-amd64.tar.gz

nano ~/.bash_profile
paste this into it : export PATH=$PATH:/usr/local/go/bin
save and exit with Ctrl + x , then Y

source ~/.bash_profile
go mod init mymodule
go mod tidy
go get github.com/AlecAivazis/survey/v2
go get github.com/fatih/color

```
- سپس اسکریپت را میتوانید اجرا نمایید.
  </details>
</div>

 ------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/guidelines.png" width="40" alt="Image"> </strong>پیش نیازها</summary>
------------------------------------ 

 - لطفا سرور اپدیت شده باشه.
 - میتوانید از اسکریپت اقای [Hwashemi](https://github.com/hawshemi/Linux-Optimizer) و یا [OPIRAN](https://github.com/opiran-club/VPS-Optimizer) هم برای بهینه سازی سرور در صورت تمایل استفاده نمایید.

------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/script.png" width="40" alt="Image">اسکریپت های کارآمد</strong></summary>
------------------------------------   



-
- این اسکریپت ها optional میباشد.


 
 Opiran Scripts
 
```
 bash <(curl -s https://raw.githubusercontent.com/opiran-club/pf-tun/main/pf-tun.sh --ipv4)
```

```
apt install curl -y && bash <(curl -s https://raw.githubusercontent.com/opiran-club/VPS-Optimizer/main/optimizer.sh --ipv4)
```

Hawshemi script

```
wget "https://raw.githubusercontent.com/hawshemi/Linux-Optimizer/main/linux-optimizer.sh" -O linux-optimizer.sh && chmod +x linux-optimizer.sh && bash linux-optimizer.sh
```


------------------------
 <div align="right">
  <details>
    <summary><strong><img src="https://github.com/69learn/6to4-azumi/blob/main/assets/119934376/script.png" width="40" alt="Image">اسکریپت من</strong></summary>
----------------
- دستور زیر فایل های پیش نیاز را نصب میکند و سپس اقدام به اجرای اسکریپت میکند. اگر مشکلی داشتید به صورت دستی هم میتوانید نصب کنید
```
sudo apt install curl -y && bash <(curl -s https://raw.githubusercontent.com/FTune12/RevTLS/main/go.sh)
```

- اگر به صورت دستی نصب کردید و پیش نیاز ها را هم دارید و میخواهید به صورت دستی هم اسکریپت را اجرا کنید میتوانید با دستور زیر اینکار را انجام دهید
```
rm tls.go
sudo apt install wget -y && wget -O /etc/logo.sh https://raw.githubusercontent.com/Azumi67/UDP2RAW_FEC/main/logo.sh && chmod +x /etc/logo.sh && wget https://raw.githubusercontent.com/FTune12/RevTLS/main/tls.go && go run tls.go
```

---------------------------------------------
