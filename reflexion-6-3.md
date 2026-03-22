### Un conflicto de merge

Un conflicto de merge es básicamente un "empate" que Git no sabe resolver solo. Ocurre cuando dos personas (o tú mismo en dos ramas distintas) modifican la misma línea de un archivo de formas diferentes, o cuando uno borra un archivo mientras el otro lo está editando. Como Git no sabe cuál versión es la "buena", se detiene y te pide que tú decidas.


### Significado de los marcadores

Git inserta estas etiquetas directamente en tu código para delimitar las versiones en disputa:


<<<<<<< HEAD: Indica el inicio del conflicto. Todo lo que esté debajo es lo que tienes actualmente en la rama donde estás parado (tu versión local).


=======: Es la línea divisoria. Separa tus cambios de los cambios que vienen de la otra rama.


>>>>>>> nombre-de-la-rama: Indica el final del conflicto. Lo que está justo arriba de esto es lo que la rama "intrusa" intenta introducir.


### Buenas prácticas para evitarlos

Para que la sangre no llegue al río, lo ideal es:


- Commits pequeños y atómicos: Es mucho más fácil resolver un conflicto en 5 líneas que en un archivo de 500 cambios.
- Hacer "Pull" frecuentemente: No te aísles. Trae los cambios de la rama principal a la tuya a diario para resolver pequeños roces sobre la marcha.
- Comunicación constante: Si vas a tocar un archivo crítico o de configuración que todos usan, avisa al equipo.
- Ramas de vida corta: Cuanto más tiempo pase una rama sin fusionarse con la principal, más posibilidades tiene de desviarse y chocar con el trabajo de otros.