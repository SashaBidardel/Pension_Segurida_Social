# Pension_Seguridad_Social :euro:
Programa escrito en lenguaje Phyton consistente en primero crear una dataframe con los datos de una serie de contribuyentes, en el que se nos pregunta primero cuántos registros queremos crear.Luego posteriormente introduciomos este dataframe en otro programa y nos calcula la pensión que les corresponde a cada registro
## Obtener csv con datos aleatórios
En el primer programa creamos el dataframe con los siguientes campos:Nombre,Apellidos,Nº Identificación,Fecha de Nacimiento,Fecha de ,JubilaciónBases de Cotización;Años Cotizados y Comunidad Autónoma.Introducimos un input en el que preguntamos cuántos registros se quieren crear.El minimo de años cotizados ha de ser 15.Como se necesitan 300 meses(25 años) para calcular la base de cotización si no se llegan a esos 25 años se rellenan con una simulación que son la base mínima (pusimos que 1000) los primeros 4 años y el resto hasta completar los 25 con la mitad de la cotización mínima(500).Para la edad de jubiación si se cotizaron 37 o más años tomamos 65 y para el resto entre 66 y 75(limitamos un poco para que no nos salgan edades ya irreales).Para las bases de cotización pusimos de mínima 1000 y máxima 3000 para ajustarnos a datos reales.Luego guardamos el data frame en un csv llamado datos_jubilacion.csv
## Obtener csv con el monto de la pensión de cada ciudadano
En el segundo programa introducimos el csv datos_jubilacion.csv y nos calcula la base reguladora que consiste en dividir la base de cotización entre 350.En los casos que se hayan trabajado 37 años o más la pensión es dicha base reguladora.En otro caso,con 15 años cotizados corresponde el 50% de la base reguladora, a partir de ahí un 0,21% por cada mes cotizado hasta los 106.Del mes 107 en adelante añadimos un 0,19% por mes.Estos datos se guardan en un csv llamado datos_jubilacion_calculados.csv