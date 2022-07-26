# NFT Generator

Автоматическая генерация крипто-артов на основе слоев изображения.

## Установка
```sh
pip3 install -r requirements.txt
```

## Как это работает
Первым делом программа рисует фон рандомного цвета, используя RGBA оттенки.
После чего используется оригинальное изображение и накладывается поверх нашего фона.
Далее извлекаются предметы персонажа из папки data/items используя их % редкости.
Всё это соединяется в 1 изображение, и каждый предмет проходит цветовую обработку,
сдвигая все пиксели в нужную позицию, чтобы цвета фона и персонажа совпадали.

Далее все готовые изображения отправляются в папку result.
Под каждого персонажа создается своя папка с его изображением и характеристиками.
В папке result/all_slimes, помещаются все изображения, чтобы было удобно ориентироваться и искать
нужного персонажа.

## Как пользоваться программой
1. Замените персонажа data/original.png на собственного.
Файл должен называться также и быть размером 2000х2000
2. Замените все предметы на свои в data/items.
Каждый предмет имеет свою редкость, поэтому самые редкие
предметы должны лежать в папке с названием 5, а предметы с шансом
выпадения в 80%, в папке 80. Они также должны быть размером 2000х2000,
формат изображения PNG и они должны заранее находится в нужной позиции.
3. Запустите генерацию персонажей - python3 main.py и укажите нужное количество
