## Проект №1:

Назвать его можно просто - **бесполезная хуйня**. Как по мне афигенное название, но на самом деле она не совсем бесполезная (для меня)

Тут я осваивал циклы while, for, работу с переменными и вводом пользователя, а так-же if, else, elif.

```python
import time

whoami = "MrCole"
id = "uid=1"
ip = "192.178.0.1"
pwd = "/home/Mr-Cole"
ls = "\n.\n..\ntext.txt"

while True:
    user = input("Введите имя пользователя: ")
    password = input("Введите пароль: ")
    if user=="MrCole" and password=="qwerty123":
        while True:
            z = input(f"{whoami}@{ip}> ")

            if z=="whoami":
                    print(whoami)
            elif z=="id":
                    print(id)
            elif z=="":
                  pass
            elif z=="pwd":
                    print(pwd)
            elif z=="ls":
                    print(ls)
            elif z=="ip a":
                    print(ip)
            elif z=="Посчитай до 10, но медленно":
                  print("Ладно!\n")
                  for i in range(1, 11):
                        time.sleep(1)
                        print(i)
                  print("Вот!\n")
            elif z=="--calc":
                  print("Запуск калькулятора...")
                  time.sleep(0.6)
                  while True:
                        number1 = int(input("Введите первое число: "))
                        number2 = int(input("Введите второе число: "))

                        time.sleep(0.5)
                        print("""Выберите одно из действий:
+ -- Сплюсовать оба числа
- -- Отнять у первого числа второе
* -- Умножить числа друг на друга
/ -- Разделить первое число на второе
""")
                        whatdoing = input("Введите действие: ")

                        result = f"{number1}{whatdoing}{number2}"

                        if whatdoing == "+" or "-" or "*" or "/":
                              print(result)

                        print("\nХотите выйти из калькулятора?")

                        nada = input("(yes/no): ")
                        if nada == "yes":
                              break
                        elif nada == "no":
                              pass
                        else:
                              print("Такого варианта нету, выход из цикла")
                              break

            elif z=="cat text.txt":
                  print("hallo lol ;D -- результат команды 'cat text.txt'")
            elif z=="exit":
                    break
            elif z=="Посчитай до 10!":
                  print("\nЗапросто, вот!\n")
                  for i in range(1, 11):
                        print(i)
                  print("")
            elif z == "help":
                print("""Список всех команд:

whoami - говорит, кто ты в системе
ip a - узнать айпи адрес
ls - увидеть содержание папки
exit - выйти
pwd - узнать, где ты находишься прямо сейчас
cat text.txt - прочитать единственный файл в системе - text.txt
Посчитай до 10! - посчитать до десяти
"Посчитай до 10, но медленно - посчитать до десяти, но медленно (разве не очевидно?)
""")
            else:
                    print("Неправильный синтаксис команды, напишите 'help' чтобы увидеть все команды")
    elif user=="exit":
           break
    else:
        print("\nНе верный логин или пароль, повторите попытку или введите 'exit' для выхода\n")
```

Относитесь к этому либо как к портфолио, либо как к какой то хрени. Мне **похуй** ;x
