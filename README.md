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
