# my-notepadpp-settings
```
compile:cmd /k cd $(CURRENT_DIRECTORY) & g++ $(FILE_NAME) -g -o $(NAME_PART).exe -Wall -std=c++11 -ftrapv & PAUSE & EXIT
compile_O2:cmd /k cd $(CURRENT_DIRECTORY) & g++ $(FILE_NAME) -g -o $(NAME_PART).exe -Wall -std=c++11 -O2 & PAUSE & EXIT
run:cmd /k cd $(CURRENT_DIRECTORY) & $(NAME_PART).exe & PAUSE & EXIT
gdb:cmd /k cd $(CURRENT_DIRECTORY) & gdb $(NAME_PART).exe & PAUSE & EXIT
compile_and_run:cmd /k cd $(CURRENT_DIRECTORY) & g++ $(FILE_NAME) -g -o $(NAME_PART).exe -Wall -std=c++11 -ftrapv & $(NAME_PART).exe & PAUSE & EXIT
```
