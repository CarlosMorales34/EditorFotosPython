RostroRecortador
Este script de Python utiliza la biblioteca OpenCV para recortar y guardar rostros detectados en fotos originales. La información de la persona asociada a cada foto se extrae de una base de datos almacenada en un archivo Excel.

Requisitos
Asegúrate de tener instaladas las siguientes bibliotecas antes de ejecutar el script:

OpenCV
OpenPyXL
Puedes instalar estas bibliotecas utilizando el siguiente comando:

bash
Copy code
pip install opencv-python openpyxl
Uso
Asegúrate de tener una base de datos de nombres en formato Excel. El script espera que la base de datos esté en el archivo base_datos_nombres/Base_datos_nombres.xlsx.

Coloca las fotos originales que deseas procesar en la carpeta Base_datos_fotos/.

Ejecuta el script. Los rostros detectados se recortarán y guardarán en la carpeta Base_datos_fotos_recortadas/.

Se generará un archivo de texto llamado nombres_errores.txt que contiene información sobre las fotos que no hicieron match o en las que no se detectaron rostros.

Detalles del Proceso
El script normaliza los caracteres de los nombres para evitar problemas con acentos y caracteres especiales.

Utiliza el clasificador de Haar de OpenCV para la detección de caras en las fotos.

Expande la región superior e inferior de cada rostro detectado antes de recortar y guardar.

El tiempo transcurrido durante el proceso se imprime al final de la ejecución.

Ten en cuenta que este script asume que las fotos originales siguen un patrón de nomenclatura que incluye un identificador único (Person ID) que se utiliza para buscar el nombre correspondiente en la base de datos.

¡Importante! Asegúrate de tener una copia de seguridad de tus datos antes de ejecutar el script, ya que modificará y creará archivos en las carpetas especificadas.
