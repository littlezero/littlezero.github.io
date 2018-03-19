# Cách sử dụng Terminator

Bạn đã chán sử dụng Terminal? Bạn cảm thấy khi phải làm việc trên nhiều tab của
Terminal thật là bất tiện, hãy đến với Terminator mọi rắc rối của bạn sẽ được
giải quyết!

## Agenda
- [x] Installation 
- [x] Same color as terminal
- [ ] Copy content to clipboard
- [ ] Config in .dotfile. What is the dotfile?
- [ ] Color like Bien

## Cài đặt
```bash
sudo apt-get update
sudo apt-get install terminator
```

## Cấu hình cho đẹp, dễ nhìn
Khi mới cài, cài đặt mặc định của Terminator sẽ rất khó nhìn với font nhỏ, chữ
mờ. Do đó cần thay đổi một chút.

### Cấu hình bằng giao diện 
```
Chuột phải > Preferences
```

### Cấu hình bằng file config

Để xem hướng dẫn cấu hình của Terminator 
```shell
man terminator_config
```
> note: `man` is the interface to view the system's references manuals
> [link](https://www.tutorialspoint.com/unix_commands/man.htm)

```
[global_config]
  inactive_color_offset = 1.0
  title_font = Sans 12
  title_hide_sizetext = True
  title_inactive_bg_color = "#ffffff"
  title_use_system_font = False
  window_state = maximise
[keybindings]
[layouts]
  [[default]]
    [[[child1]]]
      parent = window0
      profile = default
      type = Terminal
    [[[window0]]]
      parent = ""
      type = Window
[plugins]
[profiles]
  [[default]]
    background_darkness = 0.89
    background_image = None
    background_type = transparent
    copy_on_selection = True
    font = Monospace 12
    foreground_color = "#ffffff"
    palette = "#000000:#aa0000:#00aa00:#aa5500:#0000aa:#aa00aa:#00aaaa:#aaaaaa:#555555:#ff5555:#55ff55:#ffff55:#5555ff:#ff55ff:#55ffff:#ffffff"
    use_system_font = False
```

## Install Zsh
Shell mặc định trong linux là bash. Nhưng bash thì có nhược điểm là không có một số tính năng hữu ích. Vì thế sinh ra một loại shell khác là Zsh. Nhìn chung thì các chức năng cơ bản của zsh và bash là như nhau, nhưng Zsh thì "ưu việt" hơn, nhưng cũng tốn thời gian để migrate config từ bash sang zsh hơn. 

Install
```bash
apt-get install zsh
```

## Install Oh-my-zsh
Oh-my-zsh là một plugin tích hợp vào zsh để làm "màu" cho shell. Làm "màu" có quan trọn không? Xin thưa, nếu code đủ lâu thì nhìn màu cũng rất quan trọng.

Install
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

That's it! Giờ chỉ việc tắt Terminator đi và bật lại là mọi thứ ngon ngẻ.

## Tham khảo
https://viblo.asia/p/terminal-bot-te-nhat-va-de-su-dung-voi-terminator-va-zsh-tren-ubuntu-pDOKjkrXzPr
https://github.com/robbyrussell/oh-my-zsh

