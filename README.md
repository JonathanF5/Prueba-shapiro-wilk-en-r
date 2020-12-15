Prueba-shapiro-wilk-en-r

#Métodos de Regresión

#Nombre: Jonathan Calvopiña Merchan

#Cod: 59

#NORMALIDAD

#DEMOSTRAR SI ES O NO UNA NORMALIDAD
SE A TOMA COMO DATOS LAS EDADES DEL PRIMER NIVEL DE INGLES DE LA FACULTAD DE IDIOMAS
PERTENENCIENTE AL PERIODO 2014

#1)Hipotesis

#Ho:las edades se ajustan a una una distribución normal

#H1:las edades no se ajustan a una distribución normal

#2)tomo nivel de significancia

#alfa <-0.05

#edades de los alumnos del curso de ingles

edad<-c(21,20,22,25,21,21,21,21,18,25,24,23,22,24,21,21,21,26,26,24,24,25,26,27,28,18,18,19,22,23,     24,22,23,21,22,21,24,24,24,24,25,25,26,27,28,21,18,18,23)

length(edad)

#Como es una cantidad menor de 50 datos,usamos shapiro wilk

#Identifico si es una normalidad es decir si se asemeja a una distribucio normal o paprecida a una campana de gauss
#Utilizo el histograma para ver la grafica

hist(edad)

#3) 

#Aplico el test shapiro wilk

shapiro.test(edad)

#4)

#Aplico densidad y el histograma en el mismo grafico para ver como se comporta la curva

hist(edad,freq = F)

lines(density((edad)))

#El test.Shapiro >p_value es decir 0.076 >0.05,
#eso significa que no rechazo la hipotesis por ser mayor a 0.05 el p_value lo cual nos dice que si es una prueba de normalidad

#confirmo solo su densidad

plot(density(edad))

#Como podemos ver en la grafica existe 49 datos y una banda ancha de 1.106

qqnorm(edad,col= "blue")

qqline(edad,col=2)

#5)Conclusion :

#No se rechaza la hipotesis por lo que las las edades se ajustan a una una distribución normal

