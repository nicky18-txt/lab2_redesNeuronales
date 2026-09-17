## Preguntas de Discusión

1. Si la precisión en Fashion-MNIST es notablemente menor que en MNIST, ¿qué te dice eso — y qué descarta? Dado que la arquitectura, los hiperparámetros, y la semilla son idénticos, ¿puede explicarse la caída porque el modelo sea "peor"? ¿Qué debe ser diferente entonces?

    = La caida no es porque el modelo sea peor ya que es el mismo modelo que se hizo para el data set de mnist con el cual funcionó muy bien. Asimismo al tener la misma arquitectura, hiperparametros y semilla se puede deducir que al ser el dataset lo unico que cambia este seria el factor determinante y esto lo confirmo que con MNIST obtuve un 97.80% de precisión, sin embargo con Fashion MNIST obtuve un 88%. Este dataset es sobre piezas de ropa lo cual hizo que fuera mas dificil la tarea distinguir cada tipo sin una noción de vecindad ya que se aplanó a comparacion con MNIST que son digitos.

2. Observa tus dos curvas de pérdida una junto a la otra. ¿El modelo de Fashion-MNIST alcanza una pérdida de entrenamiento tan baja como la del modelo de MNIST? ¿Qué sugiere eso sobre qué tan bien una red densa aplanada, basada solo en píxeles, puede representar formas de ropa en comparación con formas de dígitos?

    = No, fashion MNIST llega a una perdida aproximada de 0.27 mientras que MNIST llega aproximadamente a 0.02 en la última época. Esto significa que se le hace mas dificil representar piezas de ropa en comparación con la forma de digitos cuando es una red densa aplanada.

3. ¿Cuánto de la brecha de precisión entre la Parte 1 y la Parte 2 logró recuperar la CNN en la Parte 3? ¿La cerró por completo, parcialmente, o no la cerró en absoluto?

    = La CCN recuperó parcialmente una parte de la brecha ya que la caida entre la parte 1 y 2 fue de 9.8 puntos (de 97.80% a 88%). Esto pasa porque la dificultad de fashion mnist aun mas en cuanto a piezas parecidad como camisas, camisetas, sueteres hacia más dificil eliminar la ambiguedad sin tener esa nocion de la vecindad. 

4. Si la CNN tiene menos parámetros que la red densa pero logra mayor precisión en Fashion-MNIST, ¿qué te dice eso sobre el valor de incorporar los supuestos estructurales correctos (conectividad local, compartición de parámetros) en una arquitectura, en lugar de simplemente agregar más capacidad bruta?

    = Me hace saber que gana la CNN al tener menos parametros porque sin importar cuantos parametros tenga un modelo, sino estan bien organizados para el tipo de dato que se usan no importara si este tiene mas o menos. Ya que la red densa gasta mas parametros en aprender lo mismo por separado en vez de aprender cosas utiles en porciones pequeñas con lo cual podemos inferir que es mas importante tener una buena arquitectura que muchos parametros.

5. ¿Qué clases confunde más tu modelo? Observa específicamente Camisa, Camiseta/Top, Suéter, y Abrigo — ¿puntúan notablemente más bajo que clases como Pantalón, Sandalia, o Bolso? ¿Esto coincide con lo que esperarías simplemente al ver algunas imágenes de ejemplo de cada clase?
    = Si, camisas, camisetas y sueteres puntuo menos que el resto ya que son prendas que se parecen mucho entre si mientras que por ejemplo pantalon, sandalias, bolso entre otros si son notablemente más diferentes entre ellas.


6. Si tu accuracy general es, digamos, 90%, pero una clase tiene un F1-score bastante por debajo de eso, ¿qué oculta el número de accuracy general? ¿Por qué el accuracy general por sí solo podría ser una forma engañosa de decidir si un modelo es "suficientemente bueno" para desplegar?
    = El accuracy puede ser engañoso porque en la mayoria puedo tener una buena precision pero no garantiza que en todas asi como paso con las camisas que se obtuvo un 0.72 el cual estaba muy por debajo qeu el resto


7. ¿Esperarías que el data augmentation (rotación, traslación) ayude a distinguir Camisa de Camiseta/Top? ¿Qué tipo de confusión es esa — un problema de traslación/orientación, o algo distinto? ¿Qué implica tu respuesta sobre qué técnicas probablemente ayuden con qué tipos de errores?
    = No porque en si esto no pasa porque las imagenes esten dadas vueltas sino porque en general esas prendas se parecen mucho entre ellas por lo cual no es un problema de orientacion o posicion. Data augmentation es para otro tipo de problemas, asi como objetos movidos o rotados, no cuando hay similitudes.
