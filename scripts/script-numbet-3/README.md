## Проект №3 - таблицы. Точнее, их изучение

Тут я решил изучать таблицы потому что.. потому что! Так вот, я решил написать простенькую программу, которая спрашивает какую песню добавить в плейлист:

```python
playlist = []

while True:
    print("Какой трек вы хотите добавить?\n")
    nane = input("Название: ").strip()

    if nane!="":
        print(f"Трек {nane} Успешно занесён в базу данных")
        playlist.append(nane)
    else:
        print("\nОшибка! Введите название трека, а не пустой знак")
        continue

    print("Хотите выйти из цикла или увидеть текущие треки в массиве?")

    wannastop = input("yes/no/show: ").strip().lower()

    if wannastop == "yes":
        break
    elif wannastop == "no":
        pass
    elif wannastop == "show":
        print("\n--- Твой плейлист ---")
        for index, item in enumerate(playlist, 1):
            print(f"{index}. {item}")
    else:
        print("Ошибка в синтаксисе! продолжение добавления")
```

Бесполезная? Да, а опыт ценный. Может однажды скрипты получше буду писать
