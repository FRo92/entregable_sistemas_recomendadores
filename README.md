### entregable_sistemas_recomendadores
Entregable  de comentarios y aportes a las últimas 3 clases de sistemas recomendadores.

# Estudiante:

Francisca Rojas Martínez

## Clase 6 - User Centric y FAccT ##

Los sistemas recomendadores pueden verse afectados por el sesgo intrínseco en los datos ocupados para el entrenamiento de los mismos. Algunos ejemplos mencionados en clases: sistema COMPAS para predicir reincidencia en delitos, sesgo de género en sistemas faciales, etc, ya que estos se basan en optimizar métricas de presición y ranking y no en justicia algorítica, ya que además es difícil de pidentificar.

En otros casos, algunos sistemas recomendadores están optimizados mediante el uso del sistema "implicit feedback". Por la forma de construcción, solo podemos hacer clic en las cosas que se nos muestran y no se tiene la oportunidad de probar productos nuevos, o también, aprenden a reforzar sus propios sesgos, lo que genera profecías autocumplidas y/o soluciones poco óptimas.
Por ejemplo, una recomendación de surtido en retail, donde los usuarios son las tiendas y los items los productos de surtido, impedirá a las tiendas probar productos nuevos que no hayan sido incluidos en las tiendas de mayor similaridad (las que incluso pueden ser de carácter socio-demográfico y no de surtido), condenando a los clientes de esa tienda a vivir una experiencia de compra repetitiva y poco novedosa.

El sesgo se puede clasificar en tres principales tipos:
* Sesgo estadístico: desviación sistemática significativa de una posible distribución desconocida.
* Sesgo Cultural: Fenómeno de interpretación y juicios adquiridos a través de nuestras experiencias y formas de vida.
* Sesgo Cognitivo:  Patrón sistmático de desviación de la norma o racionalidad en un juicio.

¿Cómo medir, estudiar y prevenir el sesgo en sistemas recomendadores?
Los lineamientos para esto se rigen por la sigla FAT: Fairness (propiedad de ser justo o equitativo), Accountability (propiedad de poder ser explicable o justificar decisiones, XAI) y Transparency (los factores que influencianlas decisiones hechas por los modelos deben ser visibles para los usuarios)

Existen varios intentos por intentar explicar los modelos de machine learning, uno de los métodos más útiles y usados es el de feature importance, pero si profundizamos un poco los métodos pasando a deep learning o sistemas recomendadores con vectores latentes ya no es posible identiicar claramente el peso de cada feature, las representaciones visuales vienen, en parte, a tratar de remediar esta situación:


## Clase 8 - Interactive and conversational recommender systems ##

