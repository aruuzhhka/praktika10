# praktika10
import pandas as pd
# Создаем датасет о миллиардерах Forbes
data = {
    'Имя': ['Илон Маск', 'Джефф Безос', 'Бернар Арно', 'Уоррен Баффет'],
    'Возраст': [50, 58, 72, 91],
    'Страна': ['США', 'США', 'Франция', 'США'],
    'Источник_богатства': ['SpaceX, Tesla', 'Amazon', 'LVMH', 'Berkshire Hathaway'],
    'Состояние ($B)': [152, 161, 146, 102]
}
df = pd.DataFrame(data)
# Выводим датасет
print(df)



import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
# Создание массива значений X от -5 до 5
X = np.linspace(-5, 5, 100)
# Определение уравнения Y = X^2
Y = X**2
# Создание фрейма данных с колонками "X" и "Y"
df = pd.DataFrame({'X': X, 'Y': Y})
# Построение графика с использованием данных из фрейма данных
plt.figure(figsize=(8, 6))
plt.plot(df['X'], df['Y'], label='Y = X^2', color='b')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('График уравнения Y = X^2 с Pandas')
plt.grid(True)
plt.legend()
# Отображение графика
plt.show()



# Создаем список состоятельности миллиардеров Forbes
состоятельность_миллиардеров = [152, 161, 146, 102, 135, 118, 125, 99, 170, 95]
# Находим самого богатого и самого "скромного" миллиардера
самый_богатый = max(состоятельность_миллиардеров)
самый_скромный = min(состоятельность_миллиардеров)
# Выводим результат
print("Самый богатый миллиардер имеет состояние в размере $", самый_богатый, "миллиардов.")
print("Самый 'скромный' миллиардер имеет состояние в размере $", самый_скромный, "миллиардов.")




import pandas as pd
# Создаем датасет о миллиардерах
forbes_data = {
    'Rank': [1, 2, 3, 4, 5],
    'Name': ['Jeff Bezos', 'Elon Musk', 'Bernard Arnault', 'Bill Gates', 'Mark Zuckerberg'],
    'Net_Worth_Billion_USD': [177, 151, 150, 120, 96],
    'Industry': ['Technology', 'Automotive', 'Fashion', 'Technology', 'Technology'],
    'Age': [58, 50, 72, 66, 37]
}
# Создаем DataFrame из датасета
forbes_df = pd.DataFrame(forbes_data)
# Выводим первые 5 строк датасета
print("Исходный датасет:")
print(forbes_df.head()
# Сохраняем датасет в CSV-файл
forbes_df.to_csv("forbes_data.csv", index=False)
# Считываем датасет из CSV-файла
read_forbes_data = pd.read_csv("forbes_data.csv")
# Выводим первые 5 строк считанного датасета
print("\nДатасет после считывания:")
print(read_forbes_data.head())
