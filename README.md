# entregable_sistemas_recomendadores
Entregable  de comentarios y aportes a las últimas 3 clases de sistemas recomendadores.

### Estudiante:

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

Existen varios intentos por intentar explicar los modelos de machine learning, uno de los métodos más útiles y usados está basado en la feature importance (por ejemplo [shap](https://shap.readthedocs.io/en/latest/)), pero si profundizamos un poco los métodos pasando a deep learning o sistemas recomendadores con vectores latentes ya no es posible identiicar claramente el peso de cada feature, las representaciones visuales vienen, en parte, a tratar de remediar esta situación ya que pueden desempeñar un papel importante en los sistemas de recomendación, ayudando a los usuarios a entender mejor cómo funciona el sistema, a interactuar con él de manera más efectiva y dar luces sobre posibles sesgos en los resultados del modelo.

Un caso curioso es el esparcimiento de fake news, ya que, dado el sesgo de confirmación, cada usuario tiende a compartir noticias o videos recomendados en RRSS que apoyen o sean afines a su ideología o perspectivas en torno a alguna problemática. Esto favorece el esparcimiento de noticias falsas como una reacción en cadena, y desde el deep learning se trabajó en un [modelo de grafo](https://paperswithcode.com/paper/user-preference-aware-fake-news-detection) que pretende detectar este tipo de comportamiento ayudandose en la estructura de grafo, características del usuario e historial de post e interacciones del mismo. Finalmente se pudo llegar a un modelo capaz de predecir con una alta precisión y valor-f (~97% ambas) aquellas noticias que son falsas.

## Clase 8 - Interactive and conversational recommender systems ##

En esta clase vimos que los sistemas de recomendación conversacionales son aquellos que utilizan el lenguaje natural para interactuar con los usuarios y brindar recomendaciones personalizadas refinada a través de las críticas, donde el principal desafío es poder representar los diálogos y las preferencias del usuario. Estos sistemas se basan en la idea de que el lenguaje natural es una forma más natural y cómoda para que los usuarios expresen sus preferencias y necesidades, y para que el sistema pueda brindar recomendaciones de manera más precisa y relevante.

Existen principalmente tres tipos de sistemas:
* 1) Sistema Activo, Usuario Pasivo (SAUP) donde el sistema pregunta y el usuario responde, funciona como un árbol de decisión para generar la recomendación.
* 2) Sistema Activo, Usuario Participativo (SAUE) donde el usuario pregunta y chatea, mientras que el sistema chatea y responde.
* 3) Sistema Activo, Usuario Activo (SAUA) donde el sistema pregunta y el usuario chatea y pregunta.

Los sistemas recomendadores conversacionales abren una gran oportunidad en el dominio de costumer care, por ejemplo, la empresa de tecnología https://www.liveperson.com/ ha anunciado la incorporación de IA conversacional tanto de texto como de voz ([Curiosly Human](https://www.liveperson.com/blog/curiously-human-conversational-ai/)) para mejorar las soluciones de interacción con clientes aprovechando las casi mil millones de interacciones al mes de la compañía, con el foco de creación de valor al tiempo que se reducen los costos de la atención tradicional.

Esto presenta una gran oportunidad de mejora en para la realidad local, puesto que constantemente se promueve la compra omnicanal, principalmente por medio de aplicaciones móviles o por la web, sin embargo, el proceso de post compra sigue fuertemente dependiente de capacidades físicas de equipos de teleperformance muy reducidos y horarios de atención acotados, servicio poco coherente con las facilidades de compra, así, soluciones basadas en tecnología abren la oportunidad de mejora de experiencia de cliente, disminuyendo las fricciones post compra especialmente en retail.

## Clase 9 - Dominios de aplicación e investigación reciente ##

En esta clase vimos un resumen de los contenidos revisados a lo largo del curso:
* Filtrado colaborativo 
* Filtrado basado en contenido
* Métodos latentes
* Usos de DL en sistemas recomendadores

Y algunos problemas:
* Filtros Burbuja (falta de exposición a contenido diverso)
* La inteligencia de la IA (no es tan inteligente para las tareas humanas que son simples)
* Falta de control y transparencia para el usuario
* ¿Son las recomendaciones justas? (FAT)
* Métricas usadas para entrenar y evaluar 
* Interactividad y múltiples fuentes de datos
* Reproducibilidad de resultados
* Conductismo (aprendiendo a partir sólo de conducta de usuario)
* No están hechos para usuarios no tradicionales
* Privacidad

Además se revisó el uso de GNNs (GCNN, Gated-GNN y GAT) para recomendación, ya que pueden procesar y analizar datos relacionales de manera efectiva. Por ejemplo, si se tiene un conjunto de datos de usuarios y productos que han sido comprados juntos, una GNN podría utilizar esa información para hacer recomendaciones a los usuarios basadas en lo que han comprado otros con intereses similares. Las GNN también pueden utilizar información sobre las relaciones entre los nodos para hacer recomendaciones más precisas y personalizadas, este tipo de redes es especialmente aplicables en estructuras de datos del tipo RRSS.

Por ejemplo, [LinkedIn utiliza las GNN](https://venturebeat.com/ai/linkedin-and-intel-tech-leaders-on-the-state-of-ai/) para hacer recomendaciones en redes sociales y comprender las relaciones entre las habilidades de las personas, intereses y sus puestos de trabajo, en particular, ha creado un proceso que denomina estrategia de muestreo adaptativo al rendimiento (PASS). Esta estrategia utiliza la IA para seleccionar a los vecinos más relevantes en los gráficos basado en sus atributos, mejorando así la precisión de la recomendación. 

También puede ayudar a detectar si uno de estos vecinos es en realidad un bot o una cuenta falsa determinando la autenticidad de sus conexiones. Este modelo adaptativo aprende a seleccionar vecinos que aumentan su precisión.

Por otra parte, se revisó el modelo GraphSAGE (I, II y III), método inductivo que permite entregar representaciones a nuevos nodos sin tener que haber entrenado con estos, ya que usa la información agregada de los vecinos. NGCF (aplica transformacione de features que se aprenden) y LightGCN (elimina parámetros de las capas de NGCF apelando a la robustez de los embeddings item-usuarios), donde se retoma la idea de representar nodos como vectores, replicando el método de filtrado colaborativo basado en usuarios e items.
