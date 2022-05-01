# Grafico-multiplas-linhas
Gerando um gráfico de múltiplas linhas com o Gapminder dataset.
# Criação de um gráfico com as bibliotecas Pandas e Plotly para a visualização de dados da expectaiva de vidas dos países do Continente Americano entre 1957-2007:
import plotly.express as px

import pandas as pd

df = px.data.gapminder().query('continent == "Americas"')

title = 'Expectativa de vida no continente Americano (1957-2007)'

fig = px.line(df, x = 'year', y= 'lifeExp', title = title, color = 'country',
             
width = 800,
             
height = 400
             
)
            
fig.update_layout(xaxis = dict(title = 'Ano'),

yaxis = dict(title = 'Expectativa de vida'),
                 
plot_bgcolor = 'white')

fig.show()

![image](https://user-images.githubusercontent.com/98922466/166165481-67af0683-9d22-4a31-be49-fdfdb9c000b1.png)
