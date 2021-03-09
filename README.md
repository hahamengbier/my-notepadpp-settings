# my-settings

## notepadpp
```
compile:cmd /k cd $(CURRENT_DIRECTORY) & g++ $(FILE_NAME) -g -o $(NAME_PART).exe -Wall -std=c++11 -ftrapv & PAUSE & EXIT
compile_O2:cmd /k cd $(CURRENT_DIRECTORY) & g++ $(FILE_NAME) -g -o $(NAME_PART).exe -Wall -std=c++11 -O2 & PAUSE & EXIT
run:cmd /k cd $(CURRENT_DIRECTORY) & $(NAME_PART).exe & PAUSE & EXIT
gdb:cmd /k cd $(CURRENT_DIRECTORY) & gdb $(NAME_PART).exe & PAUSE & EXIT
compile_and_run:cmd /k cd $(CURRENT_DIRECTORY) & g++ $(FILE_NAME) -g -o $(NAME_PART).exe -Wall -std=c++11 -ftrapv & $(NAME_PART).exe & PAUSE & EXIT
```

## vim
```
set nu
set si
set sc
set is
set cin
set ts=4
set sw=4
set sts=4
set mouse=a
set mp=g++\ -o\ -Wall\ %<\ %\ -std=c++17\ -DLOCAL

map <F9> <esc>:make<CR>
map <F10> <esc>:!./%<CR>

map <c-up> <c-y>
map <c-down> <c-e>
imap <c-up> <esc><c-y>a
imap <c-down> <esc><c-e>a
```

## emacs
```
;";"是引用
;0表示不启用,t表示启用
;可以使用Alt+x eval-buffer来观察配置文件效果
(menu-bar-mode 0);菜单栏
(tool-bar-mode 0);工具栏
(show-paren-mode t);括号匹配(高亮)
(global-linum-mode t);显示行号
(electric-pair-mode t);自动补全
(setq linum-number-mode t);下方的一小条显示光标行号
(setq column-number-mode t);下方的一小条显示光标列号
(setq linum-format "%3d| ");设置显示行号格式
(setq c-default-style "linux");设置大括号换行的样子
(set-background-color "black");背景颜色
(set-foreground-color "white");字体颜色

(setq c-basic-offset 4)
(setq default-tab-width 4)
(setq-default indent-tab-mode t)
(defun my-compile()
  (interactive)
  (save-buffer)
  (compile (format "g++ %s -g -o %s -Wall -std=c++11 -ftrapv" (buffer-file-name) (substring buffer-file-name 0 -4))))
(defun my-compile-O2()
  (interactive)
  (save-buffer)
  (compile (format "g++ %s -g -o %s -Wall -std=c++11 -O2" (buffer-file-name) (substring buffer-file-name 0 -4))))
(global-set-key [f9] 'my-compile);编译
(global-set-key [f10] 'my-compile-O2);O2编译
(global-set-key [f12] 'shell);打开shell
```

```
(menu-bar-mode 0)
(tool-bar-mode 0)
(show-paren-mode t)
(global-linum-mode t)
(electric-pair-mode t)
(setq linum-number-mode t)
(setq column-number-mode t)
(setq linum-format "%3d| ")
(setq c-default-style "linux")
(custom-set-variables  '(custom-enabled-themes (quote (adwaita))))
(set-foreground-color "white")
(set-background-color "black")
(custom-set-faces
 '(region ((t (:foreground "white" :background "#222222"))) t)
 '(fringe ((t (:foreground "white" :background "#111111"))) t)
 '(mode-line ((t (:foreground "white" :background "#222222"))) t)
 '(mode-line-inactive ((t (:foreground "#666666" :background "#111111"))) t)
 )
(set-default-font "Consolas-12")

(setq c-basic-offset 4)
(setq default-tab-width 4)
(setq-default indent-tab-mode t)
(defun find-file-yxy()
  (interactive)
  (find-file (format "~/../yxy/yxy.cpp")))
(defun find-file-std()
  (interactive)
  (find-file (format "~/../yxy/std.cpp")))
(defun find-file-data()
  (interactive)
  (find-file (format "~/../yxy/data.cpp")))
(defun find-file-test()
  (interactive)
  (find-file (format "~/../yxy/test.cpp")))
(defun my-compile()
  (interactive)
  (save-buffer)
  (compile (format "g++ %s -g -o %s -Wall -std=c++11 -ftrapv" (buffer-file-name) (substring buffer-file-name 0 -4))))
(defun my-compile-O2()
  (interactive)
  (save-buffer)
  (compile (format "g++ %s -g -o %s -Wall -std=c++11 -O2" (buffer-file-name) (substring buffer-file-name 0 -4))))
(global-set-key [f5] 'find-file-yxy)
(global-set-key [f6] 'find-file-std)
(global-set-key [f7] 'find-file-data)
(global-set-key [f8] 'find-file-test)
(global-set-key [f9] 'my-compile)
(global-set-key [f10] 'my-compile-O2)
(global-set-key [f12] 'shell)
```
