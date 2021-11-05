# II-MundosVirtuales

## 1. Qué funciones se pueden usar en los scripts de Unity para llevar a cabo traslaciones, rotaciones y escalados.
Transform.Translate, transform.Rotate y transform.localScale
## 2. ¿Cómo duplicarías el tamaño de un objeto en en un script?.
transform.localScale = new Vector3(transform.localScale.x +1 , transform.localScale.y +1 , transform.localScale.y +1);
## 3. Cómo situarías un objeto en la posición (3,5,1.)
transform.position = new Vector3(3, 5, 1)
## 4. Como trasladarías 3 metros en cada uno de los ejes y luego lo rotas 30º alrededor del eje Y?
transform.position = new Vector3(transform.position.x + 3, transform.position.y + 3, transform.position.z + 3); 
transform.rotation = Quaternion.Euler(tranform.rotation.x, transform.rotation.y + 30, transform.rotation.z);
## 5. Como rotarías un objeto sobre el eje (1,1,1)
transform.rotation = Quaternion.Euler(1, 1, 1);
## 6. Rota un objeto alrededor del eje Y 30ª y desplázalo 3 metros en cada uno de los ejes. ¿Obtendrías el mismo resultado que en 4?
transform.rotation = Quaternion.Euler(tranform.rotation.x, transform.rotation.y + 30, transform.rotation.z);
transform.position = new Vector3(transform.position.x + 3, transform.position.y + 3, transform.position.z + 3); 
Si obtendría el mismo resultado.
## 7. Como puedes obtener la distancia al plano cerca del volumen de vista desde la cámara
Se puede obtener mediante los atributos Near y Far de la cámara.
## 8. Como puedes aumentar el ángulo de la cámara
Con la propiedad Field of View
## 9. Qué efecto tiene disminuir el ángulo de la cámara.
Pierdes vision de los laterales en la escena
## 10. Configura un volumen de vista que recorte objetos de la escena.
Cambiar el atributo de la cámara Field of view (por defecto a 75) a 40.
## 11. Como puedes realizar la proyección al espacio 2D
Se puede realizar el proyección mediante la matriz de proyecciones.
## 12. Especifica la rotación de los apartados 4 y 6 con la utilidad quaternion.
transform.rotation = Quaternion.Euler(tranform.rotation.x, transform.rotation.y + 30, transform.rotation.z);
## 13. ¿Como puedes averiguar la matriz de proyección en perspectiva que se ha usado para proyectar la escena al último frame renderizado?.
Con la propiedad previousViewProjectionMatrix.
## 14. ¿Como puedes averiguar la matriz de proyección en perspectiva ortográfica que se ha usado para proyectar la escena al último frame renderizado?.
Con la propiedad CalculateProjectionMatrixFromPhysicalProperties.
## 15. ¿Cómo puedes obtener la matriz de transformación entre el sistema de coordenadas local y el mundial?.
Con la propiedad worldToLocalMatrix.
## 16. Cómo puedes obtener la matriz para cambiar al sistema de referencia de vista
Con la propiedad worldToCameraMatrix.
## 17. Especifica la matriz de la proyección usado en un instante de la ejecución del ejercicio 1 de la práctica 1.
3.621179 0 0 0

0 -3.112367 -1.12335 2.521620938

0 0 -0.17983235 0.84586213

0 -0.9278512 0.0217616 10.2745075
## 18. Especifica la matriz de modelo y vista de la escena del ejercicio 1 de la práctica 1.
1 0 0 0

0 1 0 0

0 0 1 0

0 0 0 1

## 19. Aplica una rotación en el start de uno de los objetos de la escena y muestra la matriz de cambio al sistema de referencias mundial.
1 0 0 0

0 1 0 -3

0 0 -1 -10

0 0 0 -1
## 20. ¿Como puedes calcular las coordenadas del sistema de referencia de un objeto con las siguientes propiedades del Transform:?: Position (3, 1, 1), Rotation (45, 0, 45)
Con la propiedad localToWorldMatrix.
