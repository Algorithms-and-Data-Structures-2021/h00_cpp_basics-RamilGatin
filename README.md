[![Work in Repl.it](https://classroom.github.com/assets/work-in-replit-14baed9a392b3a25080506f3b7b6d57f295ec2978f6f33ec97e36a161684cbe9.svg)](https://classroom.github.com/online_ide?assignment_repo_id=4252766&assignment_repo_type=AssignmentRepo)
# Задания по основам C++ (Часть 1)

## ФИО студента
**TODO - Пожалуйста, добавьте сюда свое ФИО**

## Описание заданий

Вам дано 8 заданий в виде отдельных функций.

1. `void swap_args(int* a, int* b)` - обмен значений переменных по указателю.
   
   - Требуется обрабатывать ситуации, когда указатели нулевые 
     (функция в этом случае ничего не должна делать).
   - Гарантируется, что указатели ссылаются на разные участки памяти.
   - Указатели могут ссылаться на участки памяти в стеке и куче.
    

2. `int** allocate_2d_array(int rows, int cols, int value)` - выделение памяти под двумерный динамический массив определенного 
   размера с инициализацией всех элементов одним значением.
   
   - Требуется обрабатывать некорректные значения размера массива 
     (в этом случае должен возвращаться нулевой указатель).
   - Все элементы массива должны быть инициализированы определенным значением.
    

3. `bool copy_2d_array(int ** src, int ** dst, int rows, int cols)` - копирование одного динамического двумерного массива в другой.
   
    - Гарантируется, что размеры массивов одинаковы.
    - Требуется обрабатывать нулевые указатели (метод должен вернуть значение `false` и ничего не делать с массивами).
    - Требуется обрабатывать некорректные значения размера массивов (неположительные значения). 
      Возвращается значение `false` и с массивами ничего не происходит.
      
4. `void reverse_1d_array(vector<int> &)` - переворот массива, все элементы должны зеркально отразиться относительно середины.
   
   - Массив может оказаться пустым.
   - Количество элементов в массиве может быть как четным, так и нечетным.
   

5. `void reverse_1d_array(int *begin, int *end)` - переворот динамического или статического массива 
   с использованием двух указателей на начальный и конечный элементы массива.
   
   - Требуется обрабатывать случай, когда указатели нулевые (функция ничего не должна делать).
   - Конечный указатель ссылается на последний элемент массива (ячейку памяти), а не на ячейку после неё.
   

6. `int *find_max_element(int *arr, int size)` - поиск максимального элемента в одномерном массиве.
   
   - Требуется обрабатывать случаи передачи нулевого указателя и неположительного размера массива.
     (в этом случае функций ничего не должна делать и вернуть нулевой указатель).
   - Функция при успешном нахождении максимального элемента должна вернуть указатель на этот элемент.


7. `vector<int> find_odd_numbers(vector<int> &)` - поиск нечетных чисел в динамическом массиве.

   - При отсутсвии нечетных элементов, возвращается пустой массив.
   - В функцию может передаваться пустой массив.
   - Требуется вернуть массив, состоящий из найденных нечетных элементов (как положительных, так и отрицательных).
   

8. `vector<int> find_common_elements(vector<int> &, vector<int> &)` - поиск общих элементов в двух динамических массивах.

   - Каждый из массивов может быть пустым.
   - Требуется вернуть массив, состоящий из общих элементов двух массивов (элементы могут быть как уникальными, так и повторяющимися).
   - При отсутствии общих элементов должен вернуться пустой массив. 

## Цели

- Все тесты должны пройти успешно:
   - для этого разрешается вносить изменения только в файлы, указанные в инструкции ниже
  
- GitHub Actions должен показывать зеленый маркер, сообщая о том, что все тесты пройдены успешно:
   - красный маркер означает, что некоторые (или все) тесты провалились
   - **Совет 1:** можно кликнуть на красный маркер, чтобы узнать какой тест провалился (или почему программа не скомпилировалась)
   - **Совет 2:** если результаты тестов не обновляются, то следует сообщить об этом преподавателю

## Инструкции

1. Добавьте свое ФИО в файл `README.md` (файл, который Вы сейчас читаете).
2. Приведите решения к заданиям в файле [`src/tasks.cpp`](src/tasks.cpp).

**Остальные файлы изменять нельзя!**

Структура проекта:
- [`src`](src) - папка с исходным кодом программы.
- [`include`](include) - папка с заголовочными файлами программы, необходима для предоставления интерфейса (API) для тестирования кода.
- [`tests`](tests) - Unit-тесты для проверки работоспособности кода.
- [`contrib`](contrib) - папка со сторонними библиотеками.
- [`CMakeLists.txt`](CMakeLists.txt) - главный файл системы автоматизации сборки проекта.

## Как запустить?

Импортируйте CMake проект в среду разработки.

Команада для клонирования репозитория в терминале:
```shell
git clone --recurse-submodules https://github.com/Algorithms-and-Data-Structures-2021/<название репозитория>
```

Для запуска всех тестов запустите исполняемый файл `run_tests`.

![Запуск всех тестов](assets/how-to-run-all-tests.png)

Запуск программы также можно осуществить через исполняемый файл `main`.


## Заметки
- Решения будут оценены лишь в том случае, если программа компилируется:
   - если код не компилируется, то оценочные тесты не будут запущены
   
- Результирующие баллы высчитываются при каждом новом коммите (до установленного дедлайна)
- Дедлайн установлен в Google Classroom (если вы его не знаете, то обратитесь к преподавателю)
