# Robot_Trading 🤖✌️

Robot Trading | Python | Data Science | Alura


#aluraChallengeRobotTrading


## Descripción 📄

Este programa en Python es capaz de tomar decisiones de compra y venta de Bitcoin en tiempo real

## Configuración del ambiente 💻

Para empezar, se puede utilizar cualquier entorno de Python, tan solo asegúrate de que sea una versión 3.X. El entorno base es Jupyter Notebook. También necesitarás instalar algunas librerías de Python que son esenciales para este proyecto, como:

- Pandas
- Numpy
- Matplotlib
- Yfinance
- Time
- BeautifulSoup
- Request
- Pycoingecko

## Obtención de datos 📃

Para la obtención de datos se recurrió al uso de la API llamada YFinance que proporciona los datos históricos de precios de Bitcoin y muchas más monedas en formato JSON. Su documentación la encontrarán en el siguiente enlace: YFinance

Por otro lado, se realiza Web Scraping en un sitio de noticias para obtener el precio actual y algunos indicadores de tendencias del Bitcoin. El sitio elegido fue: CoinMarketCap

## Limpieza de datos 🔎

Una vez se tienen los datos históricos, se cargan en un DataFrame de Pandas para poder manipularlos y analizarlos. Se identifican y eliminan los outliers, además de tratar cualquier valor nulo o duplicado en la base de datos. Finalmente, con la base limpia, se calcula el precio promedio del Bitcoin.

## Tomar decisiones ✅

Con la obtención del precio promedio, se compara con el precio actual y la tendencia del Bitcoin, que previamente se obtuvo con Web Scraping. Si el precio actual es mayor o igual que la media y la tendencia es de baja, entonces se debe vender. Si el precio actual es menor que la media y la tendencia es de alta, entonces se debe comprar. Si ninguna condición se cumple, la instrucción es esperar.

## Visualización 📊

Se utiliza la librería Matplotlib para crear un gráfico donde se muestra la evolución del precio del Bitcoin durante el periodo seleccionado, y una línea recta que pasa sobre el precio medio. Por último, se muestra un mensaje en el gráfico que indica “Vender”, “Comprar” o “Esperar” según sea la decisión del algoritmo.

![image](https://github.com/Dataerick/Robot_Tranding/assets/165416590/a9a09801-6bae-4a26-896b-fabb75965a4e)


## Automatización 🔄

Finalmente, ahora que se tienen: la extracción de información, la limpieza de datos, la visualización, y el algoritmo de decisión, es hora de automatizar el proceso. Se utiliza la librería de Python "time" para ejecutar el algoritmo de decisión cada 5 minutos y actualizar el gráfico, además del método clear_output para limpiar el gráfico antes de volver a iniciar el ciclo.

![image](https://github.com/Dataerick/Robot_Tranding/assets/165416590/f6e8cb35-6f4a-4efd-a3c1-0b78b4cf1ef9)


## Añadimos Medias Moviles 🔝

Vamos a calcular dos medias móviles: una de corto plazo (por ejemplo, 20 periodos) y otra de largo plazo (por ejemplo, 50 periodos). Esto ayudará a identificar tendencias más claramente.

Ahora vamos a ajustar la función de decisión para incluir las medias móviles en el análisis. La nueva lógica será la siguiente:

Si el precio actual está por encima de ambas medias móviles, la tendencia es alcista (compra).
Si el precio actual está por debajo de ambas medias móviles, la tendencia es bajista (venta).
En otros casos, la decisión será esperar.

![image](https://github.com/Dataerick/Robot_Tranding/assets/165416590/fef1e16c-eb86-463d-bec4-52f7da105347)

## Añadimos el RS ☑️

Vamos a actualizar la visualización para incluir el RSI en un gráfico secundario. Esto proporcionará una mejor visión del momentum del mercado.

![image](https://github.com/Dataerick/Robot_Tranding/assets/165416590/5225114e-6a19-40a9-b93d-b3bec1aa33d8)


## Desarrollador 👤

Erik Bañez Rojas

GitHub   || https://github.com/Dataerick
LinkedIn || https://www.linkedin.com/in/erik-bañez-rojas-334138291/
