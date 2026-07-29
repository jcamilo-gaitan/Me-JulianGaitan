Segundo Reporte
================
Julian Gaitan
2026-04-26

























- [1 Introducción.](#1-introducción)
- [2 Objetivo](#2-objetivo)
- [3 Pregunta problema](#3-pregunta-problema)
- [4 Parte 1: Introducción y Análisis previo de los
  datos.](#4-parte-1-introducción-y-análisis-previo-de-los-datos)
  - [4.1 `Ajuste de tipos de datos.`](#41-ajuste-de-tipos-de-datos)
  - [4.2 Modificacion de tipos de
    datos.](#42-modificacion-de-tipos-de-datos)
  - [4.3
    `Eliminación preliminar de variables.`](#43-eliminación-preliminar-de-variables)
  - [4.4 `Valores únicos`](#44-valores-únicos)
  - [4.5 `Datos nulos`](#45-datos-nulos)
  - [4.6
    `Graficos de dispersion de la variable objetivo con respecto a variables explicativas`](#46-graficos-de-dispersion-de-la-variable-objetivo-con-respecto-a-variables-explicativas)
  - [4.7
    `Graficos de dispersión entre las variables explicativas`](#47-graficos-de-dispersión-entre-las-variables-explicativas)
  - [4.8 `Evaluación de colinealidad`](#48-evaluación-de-colinealidad)
  - [4.9
    `Distribuciones de las variables categóricas`](#49-distribuciones-de-las-variables-categóricas)
  - [4.10 `Conclusiones - Parte 1`](#410-conclusiones---parte-1)
- [5 Parte 2: Estimación de modelos, ajuste y
  validación.](#5-parte-2-estimación-de-modelos-ajuste-y-validación)
  - [5.1 `Modelo Completo`](#51-modelo-completo)
  - [5.2
    `Comprobación de suspuestos del modelo completo`](#52-comprobación-de-suspuestos-del-modelo-completo)
    - [5.2.1 *1. Prueba de linealidad Y vs X - Test de
      Ramsey*](#521-1-prueba-de-linealidad-y-vs-x---test-de-ramsey)
    - [5.2.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad
      \*](#522--2-prueba-de-breusch-pagan---homocedasticidad-)
    - [5.2.3 \* 3. Prueba de autocorrelacion de los errores - Durbin
      Watson
      \*](#523--3-prueba-de-autocorrelacion-de-los-errores---durbin-watson-)
    - [5.2.4 \* 4. Prueba de normalidad de los errores- Shapiro
      \*](#524--4-prueba-de-normalidad-de-los-errores--shapiro-)
    - [5.2.5 *VIF - verificacion de inflación de varianza por
      colinealidad*](#525-vif---verificacion-de-inflación-de-varianza-por-colinealidad)
  - [5.3
    `Modelo transformado (log (precio))`](#53-modelo-transformado-log-precio)
    - [5.3.1 \* 1. Prueba de linealidad Y vs X - Test de Ramsey
      \*](#531--1-prueba-de-linealidad-y-vs-x---test-de-ramsey-)
    - [5.3.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad
      \*](#532--2-prueba-de-breusch-pagan---homocedasticidad-)
    - [5.3.3 \* 3. Prueba de autocorrelacion de los errores - Durbin
      Watson
      \*](#533--3-prueba-de-autocorrelacion-de-los-errores---durbin-watson-)
    - [5.3.4 \* 4. Prueba de normalidad de los errores- Shapiro
      \*](#534--4-prueba-de-normalidad-de-los-errores--shapiro-)
    - [5.3.5 *VIF - verificacion de inflación de varianza por
      colinealidad*](#535-vif---verificacion-de-inflación-de-varianza-por-colinealidad)
  - [5.4
    `Modelo transformado log (precio) y log(area)`](#54-modelo-transformado-log-precio-y-logarea)
  - [5.5
    `Comprobación de suspuestos del segundo modelo transformado (+log area)`](#55-comprobación-de-suspuestos-del-segundo-modelo-transformado-log-area)
    - [5.5.1 \* 1. Prueba de linealidad Y vs X - Test de Ramsey
      \*](#551--1-prueba-de-linealidad-y-vs-x---test-de-ramsey-)
    - [5.5.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad
      \*](#552--2-prueba-de-breusch-pagan---homocedasticidad-)
    - [5.5.3 \* 3. Prueba de autocorrelacion de los errores - Durbin
      Watson
      \*](#553--3-prueba-de-autocorrelacion-de-los-errores---durbin-watson-)
    - [5.5.4 \* 4. Prueba de normalidad de los errores- Shapiro
      \*](#554--4-prueba-de-normalidad-de-los-errores--shapiro-)
    - [5.5.5 *VIF - verificacion de inflación de varianza por
      colinealidad*](#555-vif---verificacion-de-inflación-de-varianza-por-colinealidad)
  - [5.6 `Modelo con pesos`](#56-modelo-con-pesos)
  - [5.7
    `Comprobación de suspuestos de modelo con pesos`](#57-comprobación-de-suspuestos-de-modelo-con-pesos)
    - [5.7.1 \* 1. Prueba de linealidad Y vs X - Test de Ramsey
      \*](#571--1-prueba-de-linealidad-y-vs-x---test-de-ramsey-)
    - [5.7.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad
      \*](#572--2-prueba-de-breusch-pagan---homocedasticidad-)
    - [5.7.3 \* 3. Prueba de autocorrelacion de los errores - Durbin
      Watson
      \*](#573--3-prueba-de-autocorrelacion-de-los-errores---durbin-watson-)
    - [5.7.4 \* 4. Prueba de normalidad de los errores- Shapiro
      \*](#574--4-prueba-de-normalidad-de-los-errores--shapiro-)
    - [5.7.5 *VIF - verificacion de inflación de varianza por
      colinealidad*](#575-vif---verificacion-de-inflación-de-varianza-por-colinealidad)
- [6 Parte 3: Exploración profunda del modelo
  final.](#6-parte-3-exploración-profunda-del-modelo-final)
  - [6.1 *Confusión*](#61-confusión)
    - [6.1.1 Resultados - confusión.](#611-resultados---confusión)
  - [6.2 *Interacción entre variables*](#62-interacción-entre-variables)
    - [6.2.1 Relacion area vs precio de acuerdo a
      estratos](#621-relacion-area-vs-precio-de-acuerdo-a-estratos)
    - [6.2.2 Relacion area vs precio de acuerdo a
      esCasa](#622-relacion-area-vs-precio-de-acuerdo-a-escasa)
    - [6.2.3 Relacion area vs precio de acuerdo a
      zona_de_lavanderia.](#623-relacion-area-vs-precio-de-acuerdo-a-zona_de_lavanderia)
  - [6.3 *Apalancamiento y análisis de observaciones
    influyentes*](#63-apalancamiento-y-análisis-de-observaciones-influyentes)
    - [6.3.1 Apalancamiento](#631-apalancamiento)
    - [6.3.2 Influencia](#632-influencia)
  - [6.4 *Selección de variables usando criterios de
    informacion*](#64-selección-de-variables-usando-criterios-de-informacion)
    - [6.4.1 Hibrido](#641-hibrido)
  - [6.5 *Validación y pronósticos del
    modelo.*](#65-validación-y-pronósticos-del-modelo)
- [7 *Interpretacion final*](#7-interpretacion-final)
  - [7.1 Rango](#71-rango)
- [8 *Conclusiones y hallazgos
  relevantes*](#8-conclusiones-y-hallazgos-relevantes)
- [9 *Recomendaciones futuras*](#9-recomendaciones-futuras)
- [10 Anexos](#10-anexos)
  - [10.1 1. Modelos calculados con estrato
    numérico:](#101-1-modelos-calculados-con-estrato-numérico)
    - [10.1.1
      `Modelo con pesos y combinaciones`](#1011-modelo-con-pesos-y-combinaciones)
    - [10.1.2 Segundo Modelo con pesos y combinaciones (con centrado de
      log(area))](#1012-segundo-modelo-con-pesos-y-combinaciones-con-centrado-de-logarea)

# 1 Introducción.

El presente conjunto de datos almacena propiedades de finca raiz en la
ciudad de bogotá, para el año 2023

# 2 Objetivo

Crear un modelo de regresión lineal múltiple para predecir el precio de
un inmueble en venta de la ciudad de Bogotá para el año 2023

# 3 Pregunta problema

¿Cual será el precio de un apartamento en venta en Bogotá para el año
2023 según sus carácterísticas inmobiliarias?

# 4 Parte 1: Introducción y Análisis previo de los datos.

En este apartado se realizarán ajustes previos al conjunto de datos.

## 4.1 `Ajuste de tipos de datos.`

    ## cols(
    ##   conjunto = col_character(),
    ##   administración = col_double(),
    ##   estrato = col_double(),
    ##   antiguedad = col_double(),
    ##   remodelado = col_character(),
    ##   área = col_double(),
    ##   habitaciones = col_double(),
    ##   baños = col_double(),
    ##   garajes = col_double(),
    ##   elevadores = col_double(),
    ##   tipo_de_inmueble = col_character(),
    ##   deposito = col_double(),
    ##   porteria = col_character(),
    ##   zona_de_lavanderia = col_character(),
    ##   gas = col_character(),
    ##   parqueadero = col_character(),
    ##   precio = col_double(),
    ##   direccion = col_character(),
    ##   nombre = col_character(),
    ##   descripcion = col_character(),
    ##   barrio = col_character()
    ## )

## 4.2 Modificacion de tipos de datos.

## 4.3 `Eliminación preliminar de variables.`

*Se eliminan variables descriptivas de los inmuebles que no tienen
relevancia en el problema*

    ##  administracion    estrato      antiguedad    remodelado      area       
    ##  Min.   :      0   1   : 15   Min.   : 0.00   No  :335   Min.   : 26.00  
    ##  1st Qu.:  74000   2   :171   1st Qu.: 7.00   Si  :247   1st Qu.: 47.00  
    ##  Median : 135000   3   :212   Median :13.00   NA's:  3   Median : 55.00  
    ##  Mean   : 205470   4   :116   Mean   :15.13              Mean   : 60.46  
    ##  3rd Qu.: 272000   5   : 47   3rd Qu.:21.00              3rd Qu.: 70.00  
    ##  Max.   :1976535   6   : 22   Max.   :48.00              Max.   :207.00  
    ##                    NA's:  2                                              
    ##   habitaciones       banos          garajes         elevadores    
    ##  Min.   :1.000   Min.   :0.000   Min.   :0.0000   Min.   :0.0000  
    ##  1st Qu.:2.000   1st Qu.:1.000   1st Qu.:0.0000   1st Qu.:0.0000  
    ##  Median :3.000   Median :2.000   Median :0.0000   Median :0.0000  
    ##  Mean   :2.593   Mean   :1.648   Mean   :0.4821   Mean   :0.5709  
    ##  3rd Qu.:3.000   3rd Qu.:2.000   3rd Qu.:1.0000   3rd Qu.:1.0000  
    ##  Max.   :8.000   Max.   :4.000   Max.   :3.0000   Max.   :4.0000  
    ##                                                                   
    ##                   tipo_de_inmueble deposito   porteria   zona_de_lavanderia
    ##  Apartamento              :547     0:473    24 hrs:540   Comunal : 54      
    ##  Casa                     :  8     1:112    No    : 45   No Tiene:531      
    ##  casa con conjunto cerrado: 30                                             
    ##                                                                            
    ##                                                                            
    ##                                                                            
    ##                                                                            
    ##    gas      parqueadero     precio         
    ##  No  :  6   No:164      Min.   :8.500e+07  
    ##  Si  :549   Si:421      1st Qu.:1.520e+08  
    ##  NA's: 30               Median :2.184e+08  
    ##                         Mean   :2.608e+08  
    ##                         3rd Qu.:3.520e+08  
    ##                         Max.   :1.530e+09  
    ## 

## 4.4 `Valores únicos`

    ## $estrato
    ## [1] 4    6    3    5    2    1    <NA>
    ## Levels: 1 2 3 4 5 6
    ## 
    ## $remodelado
    ## [1] Si   No   <NA>
    ## Levels: No Si
    ## 
    ## $tipo_de_inmueble
    ## [1] Apartamento               Casa                     
    ## [3] casa con conjunto cerrado
    ## Levels: Apartamento Casa casa con conjunto cerrado
    ## 
    ## $deposito
    ## [1] 0 1
    ## Levels: 0 1
    ## 
    ## $porteria
    ## [1] 24 hrs No    
    ## Levels: 24 hrs No
    ## 
    ## $zona_de_lavanderia
    ## [1] No Tiene Comunal 
    ## Levels: Comunal No Tiene
    ## 
    ## $gas
    ## [1] Si   <NA> No  
    ## Levels: No Si
    ## 
    ## $parqueadero
    ## [1] No Si
    ## Levels: No Si

## 4.5 `Datos nulos`

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

- En total hay 35 datos nulos en todo el conjunto de datos.
- De los 35 datos nulos la mayoría provienen de ‘gas’.
- la proporción de datos nulos sobre el conjunto total es de :
  0.0598291.

Se procede a eliminar las filas con valores nulos.

## 4.6 `Graficos de dispersion de la variable objetivo con respecto a variables explicativas`

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

No se observan relaciones no-lineales.

    ## [[1]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

    ## 
    ## [[2]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-2.png)<!-- -->

    ## 
    ## [[3]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-3.png)<!-- -->

    ## 
    ## [[4]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-4.png)<!-- -->

    ## 
    ## [[5]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-5.png)<!-- -->

    ## 
    ## [[6]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-6.png)<!-- -->

    ## 
    ## [[7]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-7.png)<!-- -->

    ## 
    ## [[8]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-8.png)<!-- -->

    ## 
    ## [[9]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-9.png)<!-- -->

    ## 
    ## [[10]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-10.png)<!-- -->

    ## 
    ## [[11]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-11.png)<!-- -->

    ## 
    ## [[12]]

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-12-12.png)<!-- -->

Se observan relacionales lineales entre las variables categoricas y el
precio usando las distribuciones de precio por cada valor categórico
como referencia.

## 4.7 `Graficos de dispersión entre las variables explicativas`

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

## 4.8 `Evaluación de colinealidad`

Se observan algunas variables explicativas que tienen correlaciones
entre sí .

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->

## 4.9 `Distribuciones de las variables categóricas`

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-15-1.png)<!-- -->

Los desbalances en variables categóricas pueden incidir en la
significancia de sus valores al momento de calcular el modelo.

## 4.10 `Conclusiones - Parte 1`

- No se observaron relaciones no-lineales de las variables explicativas
  con respecto a la variable objetivo.

- No se realizarán transformaciones de variables hasta el momento con el
  fin de conservar interpretabilidad del modelo y también teniendo en
  cuenta que se observaron relaciones lineales en el conjunto de datos.
  En la parte 2 se evaluará si es necesario transformar al comprobar los
  supuestos del modelo

- Respecto a los valores de correlación hallados, se concluye que existe
  colinealidad NO perfecta entre algunas variables. En la parte 2 se
  evaluará si es necesario retirar o transformar variables del modelo.

# 5 Parte 2: Estimación de modelos, ajuste y validación.

En este apartado se harán estimaciones de modelos, ajustes y
validaciones.

## 5.1 `Modelo Completo`

    ## 
    ## Call:
    ## lm(formula = precio ~ ., data = propiedades)
    ## 
    ## Residuals:
    ##        Min         1Q     Median         3Q        Max 
    ## -157073489  -24390346     989930   19909121  328417468 
    ## 
    ## Coefficients:
    ##                                             Estimate Std. Error t value
    ## (Intercept)                                4.134e+06  2.485e+07   0.166
    ## administracion                             1.948e+02  1.854e+01  10.506
    ## estrato2                                   1.002e+07  1.243e+07   0.806
    ## estrato3                                   3.528e+07  1.293e+07   2.728
    ## estrato4                                   7.711e+07  1.457e+07   5.291
    ## estrato5                                   7.134e+07  1.702e+07   4.192
    ## estrato6                                   7.321e+07  1.910e+07   3.832
    ## antiguedad                                -1.308e+06  2.559e+05  -5.113
    ## remodeladoSi                              -5.509e+06  4.039e+06  -1.364
    ## area                                       3.284e+06  1.959e+05  16.763
    ## habitaciones                              -1.023e+07  3.755e+06  -2.724
    ## banos                                      1.721e+07  4.605e+06   3.737
    ## garajes                                    3.021e+07  5.282e+06   5.719
    ## elevadores                                 4.712e+06  3.221e+06   1.463
    ## tipo_de_inmuebleCasa                       8.288e+07  1.744e+07   4.751
    ## tipo_de_inmueblecasa con conjunto cerrado  4.816e+06  9.389e+06   0.513
    ## depositoSi                                 1.139e+07  6.064e+06   1.878
    ## porteriaSi                                -2.179e+07  7.828e+06  -2.784
    ## zona_de_lavanderiaSi                       1.542e+07  6.907e+06   2.233
    ## gasSi                                     -4.769e+06  1.883e+07  -0.253
    ## parqueaderoSi                              1.882e+06  4.648e+06   0.405
    ##                                           Pr(>|t|)    
    ## (Intercept)                               0.867975    
    ## administracion                             < 2e-16 ***
    ## estrato2                                  0.420515    
    ## estrato3                                  0.006581 ** 
    ## estrato4                                  1.78e-07 ***
    ## estrato5                                  3.24e-05 ***
    ## estrato6                                  0.000142 ***
    ## antiguedad                                4.44e-07 ***
    ## remodeladoSi                              0.173128    
    ## area                                       < 2e-16 ***
    ## habitaciones                              0.006663 ** 
    ## banos                                     0.000206 ***
    ## garajes                                   1.79e-08 ***
    ## elevadores                                0.144057    
    ## tipo_de_inmuebleCasa                      2.61e-06 ***
    ## tipo_de_inmueblecasa con conjunto cerrado 0.608205    
    ## depositoSi                                0.060946 .  
    ## porteriaSi                                0.005567 ** 
    ## zona_de_lavanderiaSi                      0.025973 *  
    ## gasSi                                     0.800207    
    ## parqueaderoSi                             0.685772    
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 45150000 on 530 degrees of freedom
    ## Multiple R-squared:  0.9116, Adjusted R-squared:  0.9082 
    ## F-statistic: 273.1 on 20 and 530 DF,  p-value: < 2.2e-16

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-16-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-16-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-16-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-16-4.png)<!-- -->

- De acuerdo al resumen, hay algunas variables no significativas para
  estimar el precio.
- De acuerdo a ‘Residuals vs Fitted’, los residuos no tienen
  comportamiento constante a medida que aumenta el valor predicho de
  precio, podria sugerir heterocedasticidad
- De acuerdo a scale-location, puede existir heterocedasticidad porque
  los errores son menores a precios menores y viceversa.  
- De acuerdo al QQplot, podria decirse pero no afirmarse que los
  residuos NO se distrbuyen normalmente , al parecer por colas en
  valores extremos
- De acuerdo al ‘residuals vs leverage’ existen observaciones muy
  influyentes

## 5.2 `Comprobación de suspuestos del modelo completo`

<center>

### 5.2.1 *1. Prueba de linealidad Y vs X - Test de Ramsey*

</center>

$$\begin{aligned}
H_0 &: \text{El modelo está correctamente especificado (no hay variables omitidas ni no linealidad).} \\
H_1 &: \text{El modelo está mal especificado (existen variables omitidas o no linealidad).}
\end{aligned}$$

    ## 
    ##  RESET test
    ## 
    ## data:  mod
    ## RESET = 59.497, df1 = 2, df2 = 528, p-value < 2.2e-16

Se rechaza la hipótesis nula con alpha=0.05,

<center>

### 5.2.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad \*

</center>

$$
\begin{aligned}
H_0 &: \operatorname{Var}(\varepsilon_i) = \sigma^2 \quad \text{(los errores tienen varianza constante)} \\
H_1 &: \operatorname{Var}(\varepsilon_i) \neq \sigma^2 \quad \text{(existe heterocedasticidad)}
\end{aligned}
$$

    ## 
    ##  studentized Breusch-Pagan test
    ## 
    ## data:  mod
    ## BP = 227.79, df = 20, p-value < 2.2e-16

Se rechaza la hipótesis nula con alpha=0.05, no existe homocedasticidad
de los errores.

<center>

### 5.2.3 \* 3. Prueba de autocorrelacion de los errores - Durbin Watson \*

</center>

$$
\begin{aligned}
H_0 &: \rho = 0 \quad \text{(no hay autocorrelación de los errores)} \\
H_1 &: \rho \neq 0 \quad \text{(los errores están correlacionados)}
\end{aligned}
$$

    ## 
    ##  Durbin-Watson test
    ## 
    ## data:  mod
    ## DW = 2.1299, p-value = 0.9348
    ## alternative hypothesis: true autocorrelation is greater than 0

NO se rechaza la hipotesis nula de que los errores son dependientes
entre sí, se puede decir que

<center>

### 5.2.4 \* 4. Prueba de normalidad de los errores- Shapiro \*

</center>

$$
\begin{aligned}
H_0 &: \varepsilon_i \sim N(0, \sigma^2) \quad \text{(los residuos son normalmente distribuidos)} \\
H_1 &: \varepsilon_i \not\sim N(0, \sigma^2) \quad \text{(los residuos no son normales)}
\end{aligned}
$$

    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  mod$residuals
    ## W = 0.91516, p-value < 2.2e-16

Se rechaza la hipotesis nula con un nivel de significancia de 0.05 de
que el vector dado(residuales) tiene una distribución normal.

<center>

### 5.2.5 *VIF - verificacion de inflación de varianza por colinealidad*

</center>

    ##                        GVIF Df GVIF^(1/(2*Df))
    ## administracion     3.772696  1        1.942343
    ## estrato            4.344021  5        1.158215
    ## antiguedad         1.721108  1        1.311910
    ## remodelado         1.084943  1        1.041606
    ## area               4.653973  1        2.157307
    ## habitaciones       1.900581  1        1.378615
    ## banos              2.365187  1        1.537917
    ## garajes            2.918050  1        1.708230
    ## elevadores         1.593731  1        1.262431
    ## tipo_de_inmueble   1.300264  2        1.067844
    ## deposito           1.499210  1        1.224422
    ## porteria           1.114959  1        1.055916
    ## zona_de_lavanderia 1.063745  1        1.031380
    ## gas                1.032673  1        1.016205
    ## parqueadero        1.156848  1        1.075569

Ningún VIF sobrepasa 5,

En esta parte se buscará dar solución a los problemas de supuestos
encontrados en el modelo completo.

En el modelo completo se observó heterocedasticidad; tendencia al
aumento del error en función directa del aumento de precio predicho.

También observamos no - normalidad de los errores.

Por esta razón se procederá a escalar la variable precio; con el fin de
que los valores sean mas pequeños y queden en una escala común

Se procederá a eliminar del modelo las variables no significativas.

## 5.3 `Modelo transformado (log (precio))`

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ administracion + estrato + antiguedad + 
    ##     area + habitaciones + banos + garajes + elevadores + esCasa + 
    ##     zona_de_lavanderia, data = propiedades)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -0.42542 -0.09772  0.00109  0.10413  0.46361 
    ## 
    ## Coefficients:
    ##                        Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)           1.821e+01  4.891e-02 372.271  < 2e-16 ***
    ## administracion        1.952e-07  6.177e-08   3.160 0.001664 ** 
    ## estrato2              5.747e-02  4.190e-02   1.372 0.170718    
    ## estrato3              3.299e-01  4.352e-02   7.580 1.54e-13 ***
    ## estrato4              5.501e-01  4.899e-02  11.228  < 2e-16 ***
    ## estrato5              5.730e-01  5.698e-02  10.055  < 2e-16 ***
    ## estrato6              5.950e-01  6.353e-02   9.365  < 2e-16 ***
    ## antiguedad           -1.371e-03  8.427e-04  -1.627 0.104282    
    ## area                  6.755e-03  6.491e-04  10.405  < 2e-16 ***
    ## habitaciones         -1.440e-03  1.255e-02  -0.115 0.908659    
    ## banos                 1.173e-01  1.553e-02   7.552 1.86e-13 ***
    ## garajes               1.544e-01  1.758e-02   8.780  < 2e-16 ***
    ## elevadores            3.750e-02  1.070e-02   3.503 0.000499 ***
    ## esCasaSi              2.419e-01  5.772e-02   4.191 3.24e-05 ***
    ## zona_de_lavanderiaSi  5.801e-02  2.309e-02   2.513 0.012279 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.1526 on 536 degrees of freedom
    ## Multiple R-squared:  0.9107, Adjusted R-squared:  0.9084 
    ## F-statistic: 390.5 on 14 and 536 DF,  p-value: < 2.2e-16

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-22-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-22-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-22-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-22-4.png)<!-- -->

Se observan nuevas variables no significativas, se recalculará el
modelo:

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ +estrato + area + banos + garajes + 
    ##     elevadores + esCasa + zona_de_lavanderia, data = propiedades)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -0.42190 -0.09797 -0.00907  0.10398  0.48543 
    ## 
    ## Coefficients:
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          1.818e+01  4.531e-02 401.183  < 2e-16 ***
    ## estrato2             5.518e-02  4.177e-02   1.321 0.187047    
    ## estrato3             3.249e-01  4.257e-02   7.632 1.06e-13 ***
    ## estrato4             5.526e-01  4.618e-02  11.966  < 2e-16 ***
    ## estrato5             5.987e-01  5.171e-02  11.579  < 2e-16 ***
    ## estrato6             6.314e-01  5.800e-02  10.886  < 2e-16 ***
    ## area                 7.382e-03  5.161e-04  14.302  < 2e-16 ***
    ## banos                1.152e-01  1.513e-02   7.609 1.24e-13 ***
    ## garajes              1.654e-01  1.746e-02   9.474  < 2e-16 ***
    ## elevadores           4.960e-02  9.531e-03   5.204 2.77e-07 ***
    ## esCasaSi             2.057e-01  5.662e-02   3.634 0.000306 ***
    ## zona_de_lavanderiaSi 5.253e-02  2.312e-02   2.272 0.023491 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.1541 on 539 degrees of freedom
    ## Multiple R-squared:  0.9084, Adjusted R-squared:  0.9065 
    ## F-statistic: 485.9 on 11 and 539 DF,  p-value: < 2.2e-16

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-23-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-23-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-23-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-23-4.png)<!-- -->

Se ha eliminado administración porque no resultó significativa. \### \##
`Comprobación de suspuestos del modelo transformado`

<center>

### 5.3.1 \* 1. Prueba de linealidad Y vs X - Test de Ramsey \*

</center>

$$
\begin{aligned}
H_0 &: \text{El modelo está correctamente especificado (no hay variables omitidas ni no linealidad).} \\
H_1 &: \text{El modelo está mal especificado (existen variables omitidas o no linealidad).}
\end{aligned}
$$

    ## 
    ##  RESET test
    ## 
    ## data:  mod_transformado
    ## RESET = 31.922, df1 = 2, df2 = 534, p-value = 8.027e-14

Se rechaza la hipotesis nula con un nivel de significancia de 0.05,

<center>

### 5.3.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad \*

</center>

$$
\begin{aligned}
H_0 &: \operatorname{Var}(\varepsilon_i) = \sigma^2 \quad \text{(los errores tienen varianza constante)} \\
H_1 &: \operatorname{Var}(\varepsilon_i) \neq \sigma^2 \quad \text{(existe heterocedasticidad)}
\end{aligned}
$$

    ## 
    ##  studentized Breusch-Pagan test
    ## 
    ## data:  mod_transformado_rest
    ## BP = 38.418, df = 11, p-value = 6.65e-05

Se rechaza la hipótesis nula con alpha=0.05, no existe homocedasticidad
de los errores.

<center>

### 5.3.3 \* 3. Prueba de autocorrelacion de los errores - Durbin Watson \*

</center>

$$
\begin{aligned}
H_0 &: \rho = 0 \quad \text{(no hay autocorrelación de los errores)} \\
H_1 &: \rho \neq 0 \quad \text{(los errores están correlacionados)}
\end{aligned}
$$

    ## 
    ##  Durbin-Watson test
    ## 
    ## data:  mod_transformado_rest
    ## DW = 2.0711, p-value = 0.7965
    ## alternative hypothesis: true autocorrelation is greater than 0

NO se rechaza la hipotesis nula de que los errores son dependientes
entre sí, se puede decir que

<center>

### 5.3.4 \* 4. Prueba de normalidad de los errores- Shapiro \*

</center>

$$
\begin{aligned}
H_0 &: \varepsilon_i \sim N(0, \sigma^2) \quad \text{(los residuos son normalmente distribuidos)} \\
H_1 &: \varepsilon_i \not\sim N(0, \sigma^2) \quad \text{(los residuos no son normales)}
\end{aligned}
$$

    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  mod_transformado_rest$residuals
    ## W = 0.99706, p-value = 0.4272

NO se rechaza la hipotesis nula con un nivel de significancia de 0.05 de
que el vector dado(residuales) tiene una distribución normal.

<center>

### 5.3.5 *VIF - verificacion de inflación de varianza por colinealidad*

</center>

    ##                        GVIF Df GVIF^(1/(2*Df))
    ## estrato            2.541003  5        1.097743
    ## area               2.774623  1        1.665720
    ## banos              2.193744  1        1.481129
    ## garajes            2.737788  1        1.654626
    ## elevadores         1.198426  1        1.094727
    ## esCasa             1.064528  1        1.031760
    ## zona_de_lavanderia 1.024036  1        1.011947

Ningún VIF sobrepasa 5,

Para este modelo se logró pasar la prueba de normalidad gracias a la
transformación de la variable Y (precio), sin embargo el problema de
heterocedasticidad sigue presente, se intentará escalar area, para dejar
las variables numéricas en escalas similares y ver si esta variable
predictora puede estar generando esta heterocedasticidad. (Nótese que
previamente se ha eliminado administración o por no significancia)

## 5.4 `Modelo transformado log (precio) y log(area)`

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + log(area) + banos + garajes + 
    ##     elevadores + esCasa + zona_de_lavanderia, data = propiedades)
    ## 
    ## Residuals:
    ##      Min       1Q   Median       3Q      Max 
    ## -0.42151 -0.10432 -0.00575  0.09881  0.52566 
    ## 
    ## Coefficients:
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          16.453143   0.146398 112.386  < 2e-16 ***
    ## estrato2              0.066951   0.042022   1.593   0.1117    
    ## estrato3              0.320529   0.042745   7.499 2.67e-13 ***
    ## estrato4              0.552777   0.046396  11.914  < 2e-16 ***
    ## estrato5              0.598976   0.051948  11.530  < 2e-16 ***
    ## estrato6              0.642135   0.058262  11.022  < 2e-16 ***
    ## log(area)             0.541214   0.038490  14.061  < 2e-16 ***
    ## banos                 0.099364   0.015850   6.269 7.45e-10 ***
    ## garajes               0.163949   0.017615   9.308  < 2e-16 ***
    ## elevadores            0.052793   0.009582   5.510 5.57e-08 ***
    ## esCasaSi              0.226171   0.056957   3.971 8.13e-05 ***
    ## zona_de_lavanderiaSi  0.054316   0.023232   2.338   0.0198 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.1548 on 539 degrees of freedom
    ## Multiple R-squared:  0.9076, Adjusted R-squared:  0.9057 
    ## F-statistic:   481 on 11 and 539 DF,  p-value: < 2.2e-16

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-29-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-29-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-29-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-29-4.png)<!-- -->

## 5.5 `Comprobación de suspuestos del segundo modelo transformado (+log area)`

<center>

### 5.5.1 \* 1. Prueba de linealidad Y vs X - Test de Ramsey \*

</center>

$$
\begin{aligned}
H_0 &: \text{El modelo está correctamente especificado (no hay variables omitidas ni no linealidad).} \\
H_1 &: \text{El modelo está mal especificado (existen variables omitidas o no linealidad).}
\end{aligned}
$$

    ## 
    ##  RESET test
    ## 
    ## data:  mod_transformado2
    ## RESET = 0.99039, df1 = 2, df2 = 537, p-value = 0.3721

Se rechaza la hipótesis nula con alpha=0.05,

<center>

### 5.5.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad \*

</center>

$$
\begin{aligned}
H_0 &: \operatorname{Var}(\varepsilon_i) = \sigma^2 \quad \text{(los errores tienen varianza constante)} \\
H_1 &: \operatorname{Var}(\varepsilon_i) \neq \sigma^2 \quad \text{(existe heterocedasticidad)}
\end{aligned}
$$

    ## 
    ##  studentized Breusch-Pagan test
    ## 
    ## data:  mod_transformado2
    ## BP = 44.762, df = 11, p-value = 5.343e-06

Se rechaza la hipótesis nula con alpha=0.05, no existe homocedasticidad
de los errores.

<center>

### 5.5.3 \* 3. Prueba de autocorrelacion de los errores - Durbin Watson \*

</center>

$$
\begin{aligned}
H_0 &: \rho = 0 \quad \text{(no hay autocorrelación de los errores)} \\
H_1 &: \rho \neq 0 \quad \text{(los errores están correlacionados)}
\end{aligned}
$$

    ## 
    ##  Durbin-Watson test
    ## 
    ## data:  mod_transformado2
    ## DW = 2.0863, p-value = 0.8429
    ## alternative hypothesis: true autocorrelation is greater than 0

NO se rechaza la hipotesis nula de que los errores son dependientes
entre sí, se puede decir que

<center>

### 5.5.4 \* 4. Prueba de normalidad de los errores- Shapiro \*

</center>

$$
\begin{aligned}
H_0 &: \varepsilon_i \sim N(0, \sigma^2) \quad \text{(los residuos son normalmente distribuidos)} \\
H_1 &: \varepsilon_i \not\sim N(0, \sigma^2) \quad \text{(los residuos no son normales)}
\end{aligned}
$$

    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  mod_transformado2$residuals
    ## W = 0.99643, p-value = 0.256

No se rechaza la hipotesis nula con un nivel de significancia de 0.05 de
que el vector dado(residuales) tiene una distribución normal.

<center>

### 5.5.5 *VIF - verificacion de inflación de varianza por colinealidad*

</center>

    ##                        GVIF Df GVIF^(1/(2*Df))
    ## estrato            2.535046  5        1.097485
    ## log(area)          3.147193  1        1.774033
    ## banos              2.384351  1        1.544135
    ## garajes            2.760757  1        1.661552
    ## elevadores         1.200081  1        1.095482
    ## esCasa             1.067436  1        1.033168
    ## zona_de_lavanderia 1.024084  1        1.011970

Ningún VIF sobrepasa 5,

De este modelo se puede concluir que re - escalar la variable área no
fue util para lograr homocedasticidad, se realizará un modelo ponderado,
se le dará menor peso a las observaciones que generan la mayor varianza
del error

## 5.6 `Modelo con pesos`

Nota: Se trabaja con estrato como variable categórica tras encontrar que
esta transformación es favorable para el cumplimiento de los supuestos
del modelo.

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + log(area) + banos + garajes + 
    ##     elevadores + esCasa + zona_de_lavanderia, data = propiedades, 
    ##     weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.108899 -0.025778 -0.001405  0.025477  0.144198 
    ## 
    ## Coefficients:
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          16.687747   0.141120 118.252  < 2e-16 ***
    ## estrato3              0.260623   0.017352  15.020  < 2e-16 ***
    ## estrato4              0.501176   0.025458  19.687  < 2e-16 ***
    ## estrato5              0.550251   0.035860  15.345  < 2e-16 ***
    ## estrato6              0.612031   0.045869  13.343  < 2e-16 ***
    ## log(area)             0.493321   0.039264  12.564  < 2e-16 ***
    ## banos                 0.107051   0.016211   6.604 9.62e-11 ***
    ## garajes               0.168043   0.018425   9.120  < 2e-16 ***
    ## elevadores            0.054661   0.009698   5.637 2.80e-08 ***
    ## esCasaSi              0.234387   0.058894   3.980 7.84e-05 ***
    ## zona_de_lavanderiaSi  0.056773   0.023457   2.420   0.0158 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.03867 on 540 degrees of freedom
    ## Multiple R-squared:  0.8995, Adjusted R-squared:  0.8976 
    ## F-statistic: 483.1 on 10 and 540 DF,  p-value: < 2.2e-16

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-36-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-36-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-36-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-36-4.png)<!-- -->

## 5.7 `Comprobación de suspuestos de modelo con pesos`

<center>

### 5.7.1 \* 1. Prueba de linealidad Y vs X - Test de Ramsey \*

</center>

$$
\begin{aligned}
H_0 &: \text{El modelo está correctamente especificado (no hay variables omitidas ni no linealidad).} \\
H_1 &: \text{El modelo está mal especificado (existen variables omitidas o no linealidad).}
\end{aligned}
$$

    ## 
    ##  RESET test
    ## 
    ## data:  modelo_wls
    ## RESET = 0.91406, df1 = 2, df2 = 538, p-value = 0.4015

Se rechaza la hipótesis nula con alpha=0.05,

<center>

### 5.7.2 \* 2. Prueba de Breusch Pagan - Homocedasticidad \*

</center>

$$
\begin{aligned}
H_0 &: \operatorname{Var}(\varepsilon_i) = \sigma^2 \quad \text{(los errores tienen varianza constante)} \\
H_1 &: \operatorname{Var}(\varepsilon_i) \neq \sigma^2 \quad \text{(existe heterocedasticidad)}
\end{aligned}
$$

    ## 
    ##  studentized Breusch-Pagan test
    ## 
    ## data:  modelo_wls
    ## BP = 11.777, df = 10, p-value = 0.3003

NO se rechaza la hipótesis nula con alpha=0.05,

<center>

### 5.7.3 \* 3. Prueba de autocorrelacion de los errores - Durbin Watson \*

</center>

$$
\begin{aligned}
H_0 &: \rho = 0 \quad \text{(no hay autocorrelación de los errores)} \\
H_1 &: \rho \neq 0 \quad \text{(los errores están correlacionados)}
\end{aligned}
$$

    ##  lag Autocorrelation D-W Statistic p-value
    ##    1     -0.05197467      2.102149   0.234
    ##  Alternative hypothesis: rho != 0

NO se rechaza la hipotesis nula de que los errores son dependientes
entre sí, se puede decir que

<center>

### 5.7.4 \* 4. Prueba de normalidad de los errores- Shapiro \*

</center>

$$
\begin{aligned}
H_0 &: \varepsilon_i \sim N(0, \sigma^2) \quad \text{(los residuos son normalmente distribuidos)} \\
H_1 &: \varepsilon_i \not\sim N(0, \sigma^2) \quad \text{(los residuos no son normales)}
\end{aligned}
$$

    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  modelo_wls$residuals
    ## W = 0.99731, p-value = 0.5134

NO se rechaza la hipotesis nula con un nivel de significancia de 0.05 de
que el vector dado(residuales) tiene una distribución normal.

    ## Non-constant Variance Score Test 
    ## Variance formula: ~ fitted.values 
    ## Chisquare = 0.464606, Df = 1, p = 0.49548

<center>

### 5.7.5 *VIF - verificacion de inflación de varianza por colinealidad*

</center>

    ##                        GVIF Df GVIF^(1/(2*Df))
    ## estrato            2.438960  4        1.117894
    ## log(area)          2.957770  1        1.719817
    ## banos              2.336016  1        1.528403
    ## garajes            2.707409  1        1.645421
    ## elevadores         1.210897  1        1.100407
    ## esCasa             1.068231  1        1.033553
    ## zona_de_lavanderia 1.021485  1        1.010686

Ningún VIF sobrepasa 5,

EL modelo con pesos pasó todos los supuestos.

# 6 Parte 3: Exploración profunda del modelo final.

## 6.1 *Confusión*

Se obervará cúales variables existentes en el modelo son confusoras, se
usará el criterio: “Si algun coeficiente cambia más del 10%, es una
variable confusora”:

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + log(area) + banos + garajes + 
    ##     elevadores + esCasa + zona_de_lavanderia, data = propiedades, 
    ##     weights = 1/log(area)^2)
    ## 
    ## Coefficients:
    ##          (Intercept)              estrato3              estrato4  
    ##             16.68775               0.26062               0.50118  
    ##             estrato5              estrato6             log(area)  
    ##              0.55025               0.61203               0.49332  
    ##                banos               garajes            elevadores  
    ##              0.10705               0.16804               0.05466  
    ##             esCasaSi  zona_de_lavanderiaSi  
    ##              0.23439               0.05677

#### 6.1.0.1 Estrato

Se muestra la tabla comparativa, que detalla el cambio en los B´s al
quitar estrato.

    ##                                  Variable A..Sin.estrato B..Con.estrato
    ## (Intercept)                   (Intercept)    16.48967672    16.68774723
    ## log(area)                       log(area)     0.56037845     0.49332052
    ## banos                               banos     0.14655750     0.10705091
    ## garajes                           garajes     0.34475925     0.16804258
    ## elevadores                     elevadores     0.11968749     0.05466145
    ## esCasaSi                         esCasaSi     0.13529430     0.23438685
    ## zona_de_lavanderiaSi zona_de_lavanderiaSi     0.05376548     0.05677338
    ##                      Cambio..B...A.
    ## (Intercept)             0.198070516
    ## log(area)              -0.067057932
    ## banos                  -0.039506591
    ## garajes                -0.176716664
    ## elevadores             -0.065026040
    ## esCasaSi                0.099092546
    ## zona_de_lavanderiaSi    0.003007896

Se observa un cambio en el intercepto y en garajes de mas de 10%.

No se elimina ninguna variable porque todas son fundamentales para
explicar el fénomeno.

#### 6.1.0.2 log(area)

Se muestra la tabla comparativa, que detalla el cambio en los B´s al
quitar log(area).

    ##                                  Variable A..Sin.log.area. B..Con.log.area.
    ## (Intercept)                   (Intercept)      18.44373101      16.68774723
    ## estrato3                         estrato3       0.26130990       0.26062256
    ## estrato4                         estrato4       0.53068263       0.50117566
    ## estrato5                         estrato5       0.57651634       0.55025071
    ## estrato6                         estrato6       0.64128021       0.61203127
    ## banos                               banos       0.22146377       0.10705091
    ## garajes                           garajes       0.25756395       0.16804258
    ## elevadores                     elevadores       0.04870465       0.05466145
    ## esCasaSi                         esCasaSi       0.16764500       0.23438685
    ## zona_de_lavanderiaSi zona_de_lavanderiaSi       0.05044887       0.05677338
    ##                      Cambio..B...A.
    ## (Intercept)           -1.7559837753
    ## estrato3              -0.0006873447
    ## estrato4              -0.0295069737
    ## estrato5              -0.0262656304
    ## estrato6              -0.0292489408
    ## banos                 -0.1144128599
    ## garajes               -0.0895213701
    ## elevadores             0.0059568002
    ## esCasaSi               0.0667418535
    ## zona_de_lavanderiaSi   0.0063245110

Se observa un cambio del 11% en baños.

Por incompatibilidad con la naturaleza del fenómeno, no es posible
eliminar logaritmo del área

#### 6.1.0.3 Baños

Se muestra la tabla comparativa, que detalla el cambio en los B´s al
quitar baños.

    ##                                  Variable A..Sin.baños B..Con.baños
    ## (Intercept)                   (Intercept)  16.25647289  16.68774723
    ## estrato3                         estrato3   0.27875532   0.26062256
    ## estrato4                         estrato4   0.51482057   0.50117566
    ## estrato5                         estrato5   0.57140704   0.55025071
    ## estrato6                         estrato6   0.63150126   0.61203127
    ## log(area)                       log(area)   0.63896803   0.49332052
    ## garajes                           garajes   0.17369726   0.16804258
    ## elevadores                     elevadores   0.05693123   0.05466145
    ## esCasaSi                         esCasaSi   0.31165207   0.23438685
    ## zona_de_lavanderiaSi zona_de_lavanderiaSi   0.06252040   0.05677338
    ##                      Cambio..B...A.
    ## (Intercept)             0.431274338
    ## estrato3               -0.018132760
    ## estrato4               -0.013644917
    ## estrato5               -0.021156333
    ## estrato6               -0.019469986
    ## log(area)              -0.145647510
    ## garajes                -0.005654679
    ## elevadores             -0.002269772
    ## esCasaSi               -0.077265222
    ## zona_de_lavanderiaSi   -0.005747025

En este caso se observa un cambion de 40% en el intercepto (B0) y uno de
14% en log(area).

No se tomara ninguna acción porque por un lado, quitar el intercepto
puede hacer que se pierda interpretabilidad del modelo, y por el otro
lado, los baños y los garajes es una variable que, en el contexto de
negocio, es relevante en la construcción del precio de una vivienda.

Por otra parte, el área es fundamental para determinar el precio de una
vivienda.

#### 6.1.0.4 Garajes

Se muestra la tabla comparativa, que detalla el cambio en los B´s al
quitar Garajes.

    ##                                  Variable A..Sin.garajes B..Con.garajes
    ## (Intercept)                   (Intercept)    16.14949215    16.68774723
    ## estrato3                         estrato3     0.29147958     0.26062256
    ## estrato4                         estrato4     0.59479151     0.50117566
    ## estrato5                         estrato5     0.68496650     0.55025071
    ## estrato6                         estrato6     0.76034499     0.61203127
    ## log(area)                       log(area)     0.63179723     0.49332052
    ## banos                               banos     0.11392207     0.10705091
    ## elevadores                     elevadores     0.05363623     0.05466145
    ## esCasaSi                         esCasaSi     0.27291212     0.23438685
    ## zona_de_lavanderiaSi zona_de_lavanderiaSi     0.06027878     0.05677338
    ##                      Cambio..B...A.
    ## (Intercept)             0.538255087
    ## estrato3               -0.030857026
    ## estrato4               -0.093615858
    ## estrato5               -0.134715786
    ## estrato6               -0.148313716
    ## log(area)              -0.138476715
    ## banos                  -0.006871155
    ## elevadores              0.001025224
    ## esCasaSi               -0.038525276
    ## zona_de_lavanderiaSi   -0.003505404

En este caso se observa un cambio de 50% en el intercepto (B0), de 13%
aproximadamente en estrato5, estrato6 y log(area)

No se tomara ninguna acción porqu: - por un lado, quitar el intercepto
puede hacer que se pierda interpretabilidad del modelo.

- por otro lado, la cantidad de garajes es una variable que, en el
  contexto de negocio, es relevante en la construcción del precio de una
  vivienda.

- Además no es coherente remover solamente algunos estratos del modelo,
  se debe poder predecir con todos los estratos de acuerdo a la lógica
  de negocio. el área por su parte es fundamental para determinar el
  precio de una vivienda

Es decir, no se harán cambios en el modelo principal por la misma razón
que en el análisis de baños

#### 6.1.0.5 Elevadores

Se muestra la tabla comparativa, que detalla el cambio en los B´s al
quitar Elevadores.

    ##                                  Variable A..Sin.elevadores B..Con.elevadores
    ## (Intercept)                   (Intercept)       16.73425106       16.68774723
    ## estrato3                         estrato3        0.28821947        0.26062256
    ## estrato4                         estrato4        0.54269431        0.50117566
    ## estrato5                         estrato5        0.59366364        0.55025071
    ## estrato6                         estrato6        0.65524338        0.61203127
    ## log(area)                       log(area)        0.48250054        0.49332052
    ## banos                               banos        0.11028959        0.10705091
    ## garajes                           garajes        0.16683871        0.16804258
    ## esCasaSi                         esCasaSi        0.20379605        0.23438685
    ## zona_de_lavanderiaSi zona_de_lavanderiaSi        0.06854513        0.05677338
    ##                      Cambio..B...A.
    ## (Intercept)            -0.046503824
    ## estrato3               -0.027596913
    ## estrato4               -0.041518657
    ## estrato5               -0.043412930
    ## estrato6               -0.043212105
    ## log(area)               0.010819977
    ## banos                  -0.003238674
    ## garajes                 0.001203876
    ## esCasaSi                0.030590797
    ## zona_de_lavanderiaSi   -0.011771755

En este caso se observa que la cantidad de elevadores no es una variable
confusora de acuerdo al criterio empírico. “Si algun coeficiente cambia
más del 10%, es una variable confusora”

#### 6.1.0.6 esCasa

Se muestra la tabla comparativa, que detalla el cambio en los B´s al
quitar esCasa.

    ##                                  Variable A..Sin.esCasa B..Con.esCasa
    ## (Intercept)                   (Intercept)   16.72963768   16.68774723
    ## estrato3                         estrato3    0.25958004    0.26062256
    ## estrato4                         estrato4    0.49403062    0.50117566
    ## estrato5                         estrato5    0.53841460    0.55025071
    ## estrato6                         estrato6    0.59939548    0.61203127
    ## log(area)                       log(area)    0.47922618    0.49332052
    ## banos                               banos    0.11986838    0.10705091
    ## garajes                           garajes    0.17330206    0.16804258
    ## elevadores                     elevadores    0.05110494    0.05466145
    ## zona_de_lavanderiaSi zona_de_lavanderiaSi    0.05931915    0.05677338
    ##                      Cambio..B...A.
    ## (Intercept)            -0.041890445
    ## estrato3                0.001042514
    ## estrato4                0.007145033
    ## estrato5                0.011836112
    ## estrato6                0.012635792
    ## log(area)               0.014094341
    ## banos                  -0.012817471
    ## garajes                -0.005259473
    ## elevadores              0.003556510
    ## zona_de_lavanderiaSi   -0.002545771

En este caso se observa que la característica de ser una casa no es una
variable confusora de acuerdo al criterio empírico. “Si algun
coeficiente cambia más del 10%, es una variable confusora” \####
zona_de_lavanderia Se muestra la tabla comparativa, que detalla el
cambio en los B´s al quitar zona_de_lavanderia.

    ##                Variable A..Sin.zona_de_lavanderia B..Con.zona_de_lavanderia
    ## (Intercept) (Intercept)               16.69786053               16.68774723
    ## estrato3       estrato3                0.25885592                0.26062256
    ## estrato4       estrato4                0.50270057                0.50117566
    ## estrato5       estrato5                0.54593653                0.55025071
    ## estrato6       estrato6                0.61157149                0.61203127
    ## log(area)     log(area)                0.49128119                0.49332052
    ## banos             banos                0.10850662                0.10705091
    ## garajes         garajes                0.16877330                0.16804258
    ## elevadores   elevadores                0.05675117                0.05466145
    ## esCasaSi       esCasaSi                0.23827401                0.23438685
    ##             Cambio..B...A.
    ## (Intercept)  -0.0101132997
    ## estrato3      0.0017666324
    ## estrato4     -0.0015249137
    ## estrato5      0.0043141818
    ## estrato6      0.0004597846
    ## log(area)     0.0020393274
    ## banos        -0.0014557100
    ## garajes      -0.0007307150
    ## elevadores   -0.0020897191
    ## esCasaSi     -0.0038871630

En este caso se observa que la característica de tener zona de
lavanderia no es una variable confusora de acuerdo al criterio empírico.
“Si algun coeficiente cambia más del 10%, es una variable confusora”

### 6.1.1 Resultados - confusión.

En conclusión , :

- Baños: el coeficiente del intercepto (B0) cambia 40% aproximadamente.

- Garajes: el coeficiente del intercepto (B0) cambia 50%
  aproximadamente.

- Estrato: Cambios de mas de 10% en coeficientes de varias variables.

- log(area): Cambio de mas de 10% en un coeficiente de una variable.

También se pudo observar que en todos las pruebas, era el intercepto el
que más cambia.

NO se consideró eliminar alguna variable por su relevancia en el modelo,
sin embargo será útil saber que estas variables son confusoras.

## 6.2 *Interacción entre variables*

Se usará el area y el precio como principales componentes de análisis,
pues son las únicas variavles continuas del modelo

### 6.2.1 Relacion area vs precio de acuerdo a estratos

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-51-1.png)<!-- -->

Pareciera que no existe interacción entre el estrato y el area para
predecir la variable precio, no obstante se observa que la linea de
estrato 6 difiere de las demás e incluso se cruza, mientras que las
otras conservan paralelismo.

Obsérvese las proprociones:

    ## 
    ##      1 o 2          3          4          5          6 
    ## 0.33030853 0.36297641 0.19600726 0.07441016 0.03629764

Dado que todas las lineas son paralelas excepto estrato6, observemos
cómo queda el modelo tras incluir aquella interacción

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + log(area) + banos + garajes + 
    ##     log(area):I(estrato == 6) + elevadores + esCasa + zona_de_lavanderia, 
    ##     data = propiedades, weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.108871 -0.025060 -0.001207  0.024803  0.145533 
    ## 
    ## Coefficients:
    ##                                Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)                   16.581841   0.143529 115.529  < 2e-16 ***
    ## estrato3                       0.257158   0.017229  14.926  < 2e-16 ***
    ## estrato4                       0.492682   0.025362  19.426  < 2e-16 ***
    ## estrato5                       0.538614   0.035715  15.081  < 2e-16 ***
    ## estrato6                       2.165416   0.475247   4.556 6.44e-06 ***
    ## log(area)                      0.521402   0.039842  13.087  < 2e-16 ***
    ## banos                          0.105952   0.016070   6.593 1.03e-10 ***
    ## garajes                        0.166788   0.018265   9.132  < 2e-16 ***
    ## elevadores                     0.055137   0.009612   5.736 1.61e-08 ***
    ## esCasaSi                       0.231992   0.058372   3.974 8.02e-05 ***
    ## zona_de_lavanderiaSi           0.049546   0.023351   2.122  0.03431 *  
    ## log(area):I(estrato == 6)TRUE -0.359167   0.109381  -3.284  0.00109 ** 
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.03832 on 539 degrees of freedom
    ## Multiple R-squared:  0.9014, Adjusted R-squared:  0.8994 
    ## F-statistic: 448.1 on 11 and 539 DF,  p-value: < 2.2e-16

La interacción resulta significativa, pero lleva a un problema de
colinealidad:

    ##                                 GVIF Df GVIF^(1/(2*Df))
    ## estrato                   351.274517  4        2.080683
    ## log(area)                   3.100633  1        1.760861
    ## banos                       2.337029  1        1.528734
    ## garajes                     2.708594  1        1.645781
    ## elevadores                  1.211171  1        1.100532
    ## esCasa                      1.068398  1        1.033633
    ## zona_de_lavanderia          1.030643  1        1.015206
    ## log(area):I(estrato == 6) 157.998148  1       12.569731

Con este problema, esta interacción queda descartada, también teniendo
en cuenta que su aporte al ajuste del modelo no es significativo.

### 6.2.2 Relacion area vs precio de acuerdo a esCasa

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-55-1.png)<!-- -->

Se observa una interacción con esCasa, sin embargo, como se puede ver;
la mayoría de registros no son casas, lo que significa que el patron
real(poblacional) puede no está correctamente ni completamente
representado. Esto porque casi no se observan puntos para los registros
sin casa;

A continuación se observa la proporción de registros casa y no casa:

    ## 
    ##         No         Si 
    ## 0.98548094 0.01451906

No se tendrá en cuenta la interacción en el modelo por falta de
confianza estadística para determinarla.

### 6.2.3 Relacion area vs precio de acuerdo a zona_de_lavanderia.

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-57-1.png)<!-- -->
Se aprecia interacción, sin embargo sucede lo mismo que en el caso
anterior :

    ## 
    ##        No        Si 
    ## 0.9092559 0.0907441

## 6.3 *Apalancamiento y análisis de observaciones influyentes*

### 6.3.1 Apalancamiento

No se mostará el listado de observaciones con apalancamiento, pues son
bastantes y resulta dispendioso.

A continuación se muestra el apalancamiento en el conjunto de datos:

    ## # A tibble: 2 × 3
    ##   tipo              n porcentaje
    ##   <chr>         <int>      <dbl>
    ## 1 Alto leverage    50       9.07
    ## 2 Bajo leverage   501      90.9

el 9 % del conjunto de datos presenta apalancamiento, es decir: posee
carácterísticas alejadas del promedio de todos los registros (X).

### 6.3.2 Influencia

Ahora se verificará la influencia.

#### 6.3.2.1 Distancia de cook

    ## # A tibble: 551 × 4
    ##      obs   cook flag_soft flag_hard
    ##    <int>  <dbl> <lgl>     <lgl>    
    ##  1   373 0.198  TRUE      FALSE    
    ##  2   485 0.141  TRUE      FALSE    
    ##  3   474 0.0966 TRUE      FALSE    
    ##  4   486 0.0889 TRUE      FALSE    
    ##  5   447 0.0580 TRUE      FALSE    
    ##  6     5 0.0489 TRUE      FALSE    
    ##  7   309 0.0446 TRUE      FALSE    
    ##  8   383 0.0446 TRUE      FALSE    
    ##  9   354 0.0350 TRUE      FALSE    
    ## 10   479 0.0167 TRUE      FALSE    
    ## # ℹ 541 more rows

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-61-1.png)<!-- -->

Existen registros influyentes con el umbral suave.

#### 6.3.2.2 DF FITS

:)

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-62-1.png)<!-- -->

Existen observaciones influyentes

#### 6.3.2.3 COVRATIO

    ##   2   5  14  17  27  30  98  99 101 108 115 117 152 183 202 204 230 241 250 263 
    ##   2   5  14  17  27  30  98  99 101 108 115 117 152 183 202 204 230 241 250 263 
    ## 284 299 302 309 352 354 373 376 392 438 443 447 467 474 478 479 481 486 488 500 
    ## 284 299 302 309 352 354 373 376 392 438 443 447 467 474 478 479 481 486 488 500 
    ## 510 511 542 
    ## 510 511 542

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-63-1.png)<!-- -->

Existen observaciones influyentes

#### 6.3.2.4 Coinicidencias

¿Cuales son las observaciones en las cuales todos los métodos coinciden?

    ## # A tibble: 14 × 1
    ##      obs
    ##    <int>
    ##  1   373
    ##  2   474
    ##  3   486
    ##  4   447
    ##  5     5
    ##  6   309
    ##  7   354
    ##  8   479
    ##  9    98
    ## 10   478
    ## 11   443
    ## 12   250
    ## 13    14
    ## 14   117

Existen 14 registos problematicos que influyen significativamente.

    ## # A tibble: 14 × 6
    ##       precio  area estrato banos garajes esCasa
    ##        <dbl> <dbl> <fct>   <int>   <int> <fct> 
    ##  1 145800000    41 3           1       0 Si    
    ##  2 450000000    45 3           4       1 Si    
    ##  3 320000000    45 3           2       0 Si    
    ##  4 450000000    72 1 o 2       4       1 Si    
    ##  5 387000000   105 4           2       1 Si    
    ##  6 355000000    74 3           3       2 Si    
    ##  7 250000000    35 3           1       0 No    
    ##  8 490000000   126 1 o 2       3       1 Si    
    ##  9 174000000    59 3           2       0 No    
    ## 10 270000000    38 3           1       0 No    
    ## 11 440000000    59 3           2       1 No    
    ## 12 167613000    62 1 o 2       1       0 Si    
    ## 13 200000000    38 1 o 2       1       0 No    
    ## 14 142340000    49 3           1       1 No

Estas observaciones son raras (no usuales), aunque son posibles en el
estudio de este fenomeno, por dar algunos ejemplos

- Observaciones 1 y 2: es raro que dos viviendas estrato 2 de similar
  area tengan una diferencia de 300 Millones de pesos, el mas costoso
  tiene 1 garaje y dos baños mas que el otro.

- Observación 7: 250 Millones es demasiado para un apartamento de tan
  sólo 35m2 que está en un estrato 2.

- Observacion 9: No es usual encontrar viviendas de 490 Millones en el
  estrato 1 .

Estas observaciones NO seran excluidas del modelo, si bien son no -
usuales, son propias del fenomeno, es aceptable que esto suceda en la
vida real (podría suceder).

## 6.4 *Selección de variables usando criterios de informacion*

Se usarán todas las variables del modelo actual (7), se podrá determinar
si existen modelos mas pequeños que este que puedan ofrecer un ajuste
similar. \### Forward Aplicacion de la técnica stepwise:

    ## Start:  AIC=-2327.91
    ## log(precio) ~ 1
    ## 
    ##                      Df Sum of Sq    RSS     AIC
    ## + estrato             4    5.6917 2.3385 -2999.7
    ## + garajes             1    5.2174 2.8129 -2903.9
    ## + log(area)           1    5.1507 2.8796 -2891.0
    ## + banos               1    4.0730 3.9573 -2715.8
    ## + elevadores          1    1.1005 6.9298 -2407.1
    ## + zona_de_lavanderia  1    0.0715 7.9588 -2330.8
    ## + esCasa              1    0.0629 7.9674 -2330.2
    ## <none>                            8.0303 -2327.9
    ## 
    ## Step:  AIC=-2999.68
    ## log(precio) ~ estrato
    ## 
    ##                      Df Sum of Sq    RSS     AIC
    ## + log(area)           1   1.21529 1.1232 -3401.7
    ## + banos               1   0.89539 1.4431 -3263.6
    ## + garajes             1   0.78613 1.5524 -3223.4
    ## + esCasa              1   0.09966 2.2389 -3021.7
    ## + elevadores          1   0.02438 2.3141 -3003.5
    ## + zona_de_lavanderia  1   0.02124 2.3173 -3002.7
    ## <none>                            2.3385 -2999.7
    ## 
    ## Step:  AIC=-3401.74
    ## log(precio) ~ estrato + log(area)
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + garajes             1  0.146338 0.97689 -3476.6
    ## + banos               1  0.105155 1.01807 -3453.9
    ## + esCasa              1  0.050566 1.07266 -3425.1
    ## + elevadores          1  0.045968 1.07726 -3422.8
    ## + zona_de_lavanderia  1  0.018773 1.10445 -3409.0
    ## <none>                            1.12323 -3401.7
    ## 
    ## Step:  AIC=-3476.65
    ## log(precio) ~ estrato + log(area) + garajes
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + banos               1  0.090541 0.88635 -3528.2
    ## + elevadores          1  0.048553 0.92834 -3502.7
    ## + esCasa              1  0.037353 0.93954 -3496.1
    ## + zona_de_lavanderia  1  0.016770 0.96012 -3484.2
    ## <none>                            0.97689 -3476.6
    ## 
    ## Step:  AIC=-3528.24
    ## log(precio) ~ estrato + log(area) + garajes + banos
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + elevadores          1  0.045774 0.84057 -3555.5
    ## + esCasa              1  0.018653 0.86769 -3538.0
    ## + zona_de_lavanderia  1  0.013466 0.87288 -3534.7
    ## <none>                            0.88635 -3528.2
    ## 
    ## Step:  AIC=-3555.46
    ## log(precio) ~ estrato + log(area) + garajes + banos + elevadores
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + esCasa              1 0.0244901 0.81608 -3569.8
    ## + zona_de_lavanderia  1 0.0095682 0.83101 -3559.8
    ## <none>                            0.84057 -3555.5
    ## 
    ## Step:  AIC=-3569.75
    ## log(precio) ~ estrato + log(area) + garajes + banos + elevadores + 
    ##     esCasa
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + zona_de_lavanderia  1  0.008758 0.80733 -3573.7
    ## <none>                            0.81608 -3569.8
    ## 
    ## Step:  AIC=-3573.7
    ## log(precio) ~ estrato + log(area) + garajes + banos + elevadores + 
    ##     esCasa + zona_de_lavanderia

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + log(area) + garajes + banos + 
    ##     elevadores + esCasa + zona_de_lavanderia, data = propiedades, 
    ##     weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.108899 -0.025778 -0.001405  0.025477  0.144198 
    ## 
    ## Coefficients:
    ##                       Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          16.687747   0.141120 118.252  < 2e-16 ***
    ## estrato3              0.260623   0.017352  15.020  < 2e-16 ***
    ## estrato4              0.501176   0.025458  19.687  < 2e-16 ***
    ## estrato5              0.550251   0.035860  15.345  < 2e-16 ***
    ## estrato6              0.612031   0.045869  13.343  < 2e-16 ***
    ## log(area)             0.493321   0.039264  12.564  < 2e-16 ***
    ## garajes               0.168043   0.018425   9.120  < 2e-16 ***
    ## banos                 0.107051   0.016211   6.604 9.62e-11 ***
    ## elevadores            0.054661   0.009698   5.637 2.80e-08 ***
    ## esCasaSi              0.234387   0.058894   3.980 7.84e-05 ***
    ## zona_de_lavanderiaSi  0.056773   0.023457   2.420   0.0158 *  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.03867 on 540 degrees of freedom
    ## Multiple R-squared:  0.8995, Adjusted R-squared:  0.8976 
    ## F-statistic: 483.1 on 10 and 540 DF,  p-value: < 2.2e-16

Se obtiene el mismo modelo actual. \### Backwards

    ## Start:  AIC=-3573.7
    ## log(precio) ~ estrato + log(area) + banos + garajes + elevadores + 
    ##     esCasa + zona_de_lavanderia
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## <none>                            0.80733 -3573.7
    ## - zona_de_lavanderia  1   0.00876 0.81608 -3569.8
    ## - esCasa              1   0.02368 0.83101 -3559.8
    ## - elevadores          1   0.04750 0.85483 -3544.2
    ## - banos               1   0.06520 0.87252 -3532.9
    ## - garajes             1   0.12436 0.93168 -3496.8
    ## - log(area)           1   0.23601 1.04334 -3434.4
    ## - estrato             4   0.67374 1.48106 -3247.4

Se obtiene el mismo modelo actual

### 6.4.1 Hibrido

    ## Start:  AIC=-2891.01
    ## log(precio) ~ log(area)
    ## 
    ##                      Df Sum of Sq    RSS     AIC
    ## + estrato             4    1.7563 1.1232 -3401.7
    ## + garajes             1    0.9493 1.9302 -3109.4
    ## + elevadores          1    0.4521 2.4274 -2983.1
    ## + banos               1    0.2782 2.6014 -2945.0
    ## + zona_de_lavanderia  1    0.0344 2.8452 -2895.6
    ## + esCasa              1    0.0199 2.8597 -2892.8
    ## <none>                            2.8796 -2891.0
    ## - log(area)           1    5.1507 8.0303 -2327.9
    ## 
    ## Step:  AIC=-3401.74
    ## log(precio) ~ log(area) + estrato
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + garajes             1   0.14634 0.97689 -3476.6
    ## + banos               1   0.10515 1.01807 -3453.9
    ## + esCasa              1   0.05057 1.07266 -3425.1
    ## + elevadores          1   0.04597 1.07726 -3422.8
    ## + zona_de_lavanderia  1   0.01877 1.10445 -3409.0
    ## <none>                            1.12323 -3401.7
    ## - log(area)           1   1.21529 2.33852 -2999.7
    ## - estrato             4   1.75635 2.87957 -2891.0
    ## 
    ## Step:  AIC=-3476.65
    ## log(precio) ~ log(area) + estrato + garajes
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + banos               1   0.09054 0.88635 -3528.2
    ## + elevadores          1   0.04855 0.92834 -3502.7
    ## + esCasa              1   0.03735 0.93954 -3496.1
    ## + zona_de_lavanderia  1   0.01677 0.96012 -3484.2
    ## <none>                            0.97689 -3476.6
    ## - garajes             1   0.14634 1.12323 -3401.7
    ## - log(area)           1   0.57550 1.55239 -3223.4
    ## - estrato             4   0.95335 1.93024 -3109.4
    ## 
    ## Step:  AIC=-3528.24
    ## log(precio) ~ log(area) + estrato + garajes + banos
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + elevadores          1   0.04577 0.84057 -3555.5
    ## + esCasa              1   0.01865 0.86769 -3538.0
    ## + zona_de_lavanderia  1   0.01347 0.87288 -3534.7
    ## <none>                            0.88635 -3528.2
    ## - banos               1   0.09054 0.97689 -3476.6
    ## - garajes             1   0.13172 1.01807 -3453.9
    ## - log(area)           1   0.21422 1.10057 -3411.0
    ## - estrato             4   0.86903 1.75538 -3159.7
    ## 
    ## Step:  AIC=-3555.46
    ## log(precio) ~ log(area) + estrato + garajes + banos + elevadores
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + esCasa              1   0.02449 0.81608 -3569.8
    ## + zona_de_lavanderia  1   0.00957 0.83101 -3559.8
    ## <none>                            0.84057 -3555.5
    ## - elevadores          1   0.04577 0.88635 -3528.2
    ## - banos               1   0.08776 0.92834 -3502.7
    ## - garajes             1   0.13431 0.97488 -3475.8
    ## - log(area)           1   0.22245 1.06302 -3428.1
    ## - estrato             4   0.65684 1.49741 -3245.3
    ## 
    ## Step:  AIC=-3569.75
    ## log(precio) ~ log(area) + estrato + garajes + banos + elevadores + 
    ##     esCasa
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + zona_de_lavanderia  1   0.00876 0.80733 -3573.7
    ## <none>                            0.81608 -3569.8
    ## - esCasa              1   0.02449 0.84057 -3555.5
    ## - elevadores          1   0.05161 0.86769 -3538.0
    ## - banos               1   0.06707 0.88316 -3528.2
    ## - garajes             1   0.12547 0.94156 -3492.9
    ## - log(area)           1   0.23417 1.05025 -3432.7
    ## - estrato             4   0.67290 1.48899 -3246.4
    ## 
    ## Step:  AIC=-3573.7
    ## log(precio) ~ log(area) + estrato + garajes + banos + elevadores + 
    ##     esCasa + zona_de_lavanderia
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## <none>                            0.80733 -3573.7
    ## - zona_de_lavanderia  1   0.00876 0.81608 -3569.8
    ## - esCasa              1   0.02368 0.83101 -3559.8
    ## - elevadores          1   0.04750 0.85483 -3544.2
    ## - banos               1   0.06520 0.87252 -3532.9
    ## - garajes             1   0.12436 0.93168 -3496.8
    ## - log(area)           1   0.23601 1.04334 -3434.4
    ## - estrato             4   0.67374 1.48106 -3247.4

Se ha obtenido el mismo modelo.

En los tres métodos de selección se determina que, dentro del espectro
de variables propuesto, es el que mejor AIC tiene.

Ahora se intentará probar otro modelo, ampliando el espectro de
variables pero manteniendpo la estructura de pesos

    ## Start:  AIC=-2891.01
    ## log(precio) ~ log(area)
    ## 
    ##                      Df Sum of Sq    RSS     AIC
    ## + estrato             4    1.7563 1.1232 -3401.7
    ## + garajes             1    0.9493 1.9302 -3109.4
    ## + administracion      1    0.7808 2.0988 -3063.3
    ## + elevadores          1    0.4521 2.4274 -2983.1
    ## + habitaciones        1    0.4444 2.4352 -2981.4
    ## + deposito            1    0.2976 2.5819 -2949.1
    ## + banos               1    0.2782 2.6014 -2945.0
    ## + area                1    0.0467 2.8328 -2898.0
    ## + tipo_de_inmueble    2    0.0485 2.8311 -2896.4
    ## + porteria            1    0.0371 2.8425 -2896.2
    ## + zona_de_lavanderia  1    0.0344 2.8452 -2895.6
    ## + esCasa              1    0.0199 2.8597 -2892.8
    ## + gas                 1    0.0107 2.8688 -2891.1
    ## <none>                            2.8796 -2891.0
    ## + remodelado          1    0.0045 2.8751 -2889.9
    ## + parqueadero         1    0.0009 2.8786 -2889.2
    ## + antiguedad          1    0.0002 2.8793 -2889.1
    ## - log(area)           1    5.1507 8.0303 -2327.9
    ## 
    ## Step:  AIC=-3401.74
    ## log(precio) ~ log(area) + estrato
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + garajes             1   0.14634 0.97689 -3476.6
    ## + banos               1   0.10515 1.01807 -3453.9
    ## + administracion      1   0.08234 1.04089 -3441.7
    ## + esCasa              1   0.05057 1.07266 -3425.1
    ## + tipo_de_inmueble    2   0.05092 1.07231 -3423.3
    ## + elevadores          1   0.04597 1.07726 -3422.8
    ## + deposito            1   0.03548 1.08774 -3417.4
    ## + antiguedad          1   0.02562 1.09761 -3412.4
    ## + area                1   0.02462 1.09861 -3411.9
    ## + zona_de_lavanderia  1   0.01877 1.10445 -3409.0
    ## + porteria            1   0.01165 1.11158 -3405.5
    ## <none>                            1.12323 -3401.7
    ## + habitaciones        1   0.00350 1.11973 -3401.5
    ## + parqueadero         1   0.00086 1.12236 -3400.2
    ## + gas                 1   0.00033 1.12289 -3399.9
    ## + remodelado          1   0.00016 1.12307 -3399.8
    ## - log(area)           1   1.21529 2.33852 -2999.7
    ## - estrato             4   1.75635 2.87957 -2891.0
    ## 
    ## Step:  AIC=-3476.65
    ## log(precio) ~ log(area) + estrato + garajes
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + banos               1   0.09054 0.88635 -3528.2
    ## + elevadores          1   0.04855 0.92834 -3502.7
    ## + administracion      1   0.04569 0.93120 -3501.0
    ## + esCasa              1   0.03735 0.93954 -3496.1
    ## + tipo_de_inmueble    2   0.03926 0.93762 -3495.3
    ## + antiguedad          1   0.02473 0.95216 -3488.8
    ## + area                1   0.01763 0.95926 -3484.7
    ## + zona_de_lavanderia  1   0.01677 0.96012 -3484.2
    ## + deposito            1   0.01367 0.96322 -3482.4
    ## + porteria            1   0.00747 0.96941 -3478.9
    ## <none>                            0.97689 -3476.6
    ## + gas                 1   0.00051 0.97637 -3474.9
    ## + parqueadero         1   0.00030 0.97659 -3474.8
    ## + remodelado          1   0.00028 0.97660 -3474.8
    ## + habitaciones        1   0.00017 0.97672 -3474.7
    ## - garajes             1   0.14634 1.12323 -3401.7
    ## - log(area)           1   0.57550 1.55239 -3223.4
    ## - estrato             4   0.95335 1.93024 -3109.4
    ## 
    ## Step:  AIC=-3528.24
    ## log(precio) ~ log(area) + estrato + garajes + banos
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + administracion      1   0.04838 0.83797 -3557.2
    ## + elevadores          1   0.04577 0.84057 -3555.5
    ## + area                1   0.02242 0.86393 -3540.4
    ## + antiguedad          1   0.02033 0.86602 -3539.0
    ## + esCasa              1   0.01865 0.86769 -3538.0
    ## + tipo_de_inmueble    2   0.02104 0.86531 -3537.5
    ## + deposito            1   0.01360 0.87275 -3534.8
    ## + zona_de_lavanderia  1   0.01347 0.87288 -3534.7
    ## + habitaciones        1   0.00570 0.88065 -3529.8
    ## + porteria            1   0.00400 0.88235 -3528.7
    ## <none>                            0.88635 -3528.2
    ## + remodelado          1   0.00030 0.88605 -3526.4
    ## + parqueadero         1   0.00029 0.88606 -3526.4
    ## + gas                 1   0.00013 0.88622 -3526.3
    ## - banos               1   0.09054 0.97689 -3476.6
    ## - garajes             1   0.13172 1.01807 -3453.9
    ## - log(area)           1   0.21422 1.10057 -3411.0
    ## - estrato             4   0.86903 1.75538 -3159.7
    ## 
    ## Step:  AIC=-3557.17
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + elevadores          1   0.03397 0.80400 -3578.0
    ## + tipo_de_inmueble    2   0.03148 0.80649 -3574.3
    ## + esCasa              1   0.02665 0.81132 -3573.0
    ## + zona_de_lavanderia  1   0.01793 0.82004 -3567.1
    ## + antiguedad          1   0.01779 0.82018 -3567.0
    ## + deposito            1   0.01040 0.82757 -3562.0
    ## + porteria            1   0.00812 0.82985 -3560.5
    ## + area                1   0.00385 0.83412 -3557.7
    ## <none>                            0.83797 -3557.2
    ## + habitaciones        1   0.00078 0.83719 -3555.7
    ## + gas                 1   0.00042 0.83755 -3555.4
    ## + parqueadero         1   0.00023 0.83774 -3555.3
    ## + remodelado          1   0.00000 0.83797 -3555.2
    ## - administracion      1   0.04838 0.88635 -3528.2
    ## - banos               1   0.09323 0.93120 -3501.0
    ## - garajes             1   0.09640 0.93437 -3499.2
    ## - log(area)           1   0.14883 0.98680 -3469.1
    ## - estrato             4   0.66056 1.49853 -3244.9
    ## 
    ## Step:  AIC=-3577.97
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion + 
    ##     elevadores
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + tipo_de_inmueble    2   0.04156 0.76243 -3603.2
    ## + esCasa              1   0.03151 0.77249 -3598.0
    ## + zona_de_lavanderia  1   0.01348 0.79052 -3585.3
    ## + porteria            1   0.01069 0.79331 -3583.3
    ## + deposito            1   0.00683 0.79717 -3580.7
    ## + area                1   0.00401 0.79998 -3578.7
    ## <none>                            0.80400 -3578.0
    ## + antiguedad          1   0.00283 0.80117 -3577.9
    ## + habitaciones        1   0.00079 0.80321 -3576.5
    ## + parqueadero         1   0.00078 0.80322 -3576.5
    ## + gas                 1   0.00031 0.80369 -3576.2
    ## + remodelado          1   0.00024 0.80376 -3576.1
    ## - elevadores          1   0.03397 0.83797 -3557.2
    ## - administracion      1   0.03658 0.84057 -3555.5
    ## - banos               1   0.09042 0.89442 -3521.2
    ## - garajes             1   0.10154 0.90554 -3514.4
    ## - log(area)           1   0.15957 0.96356 -3480.2
    ## - estrato             4   0.52513 1.32913 -3309.0
    ## 
    ## Step:  AIC=-3603.22
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion + 
    ##     elevadores + tipo_de_inmueble
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + zona_de_lavanderia  1   0.01190 0.75053 -3609.9
    ## + deposito            1   0.00718 0.75525 -3606.4
    ## + porteria            1   0.00675 0.75568 -3606.1
    ## + antiguedad          1   0.00634 0.75609 -3605.8
    ## + habitaciones        1   0.00306 0.75937 -3603.4
    ## <none>                            0.76243 -3603.2
    ## + area                1   0.00169 0.76074 -3602.4
    ## + gas                 1   0.00045 0.76198 -3601.5
    ## + remodelado          1   0.00021 0.76222 -3601.4
    ## + parqueadero         1   0.00000 0.76243 -3601.2
    ## - tipo_de_inmueble    2   0.04156 0.80400 -3578.0
    ## - elevadores          1   0.04406 0.80649 -3574.3
    ## - administracion      1   0.04621 0.80864 -3572.8
    ## - banos               1   0.06800 0.83044 -3558.1
    ## - garajes             1   0.09352 0.85595 -3541.5
    ## - log(area)           1   0.14942 0.91185 -3506.6
    ## - estrato             4   0.53244 1.29488 -3319.4
    ## 
    ## Step:  AIC=-3609.89
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion + 
    ##     elevadores + tipo_de_inmueble + zona_de_lavanderia
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + porteria            1   0.00770 0.74283 -3613.6
    ## + deposito            1   0.00630 0.74423 -3612.5
    ## + antiguedad          1   0.00556 0.74497 -3612.0
    ## <none>                            0.75053 -3609.9
    ## + habitaciones        1   0.00238 0.74815 -3609.6
    ## + area                1   0.00118 0.74935 -3608.8
    ## + gas                 1   0.00008 0.75045 -3608.0
    ## + parqueadero         1   0.00006 0.75048 -3607.9
    ## + remodelado          1   0.00004 0.75049 -3607.9
    ## - zona_de_lavanderia  1   0.01190 0.76243 -3603.2
    ## - tipo_de_inmueble    2   0.03999 0.79052 -3585.3
    ## - elevadores          1   0.03890 0.78943 -3584.0
    ## - administracion      1   0.05005 0.80058 -3576.3
    ## - banos               1   0.06579 0.81632 -3565.6
    ## - garajes             1   0.09088 0.84141 -3548.9
    ## - log(area)           1   0.14965 0.90018 -3511.7
    ## - estrato             4   0.52894 1.27947 -3324.0
    ## 
    ## Step:  AIC=-3613.57
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion + 
    ##     elevadores + tipo_de_inmueble + zona_de_lavanderia + porteria
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + antiguedad          1   0.00651 0.73632 -3616.4
    ## + deposito            1   0.00635 0.73647 -3616.3
    ## <none>                            0.74283 -3613.6
    ## + habitaciones        1   0.00230 0.74052 -3613.3
    ## + area                1   0.00106 0.74177 -3612.4
    ## + gas                 1   0.00014 0.74269 -3611.7
    ## + parqueadero         1   0.00006 0.74277 -3611.6
    ## + remodelado          1   0.00000 0.74282 -3611.6
    ## - porteria            1   0.00770 0.75053 -3609.9
    ## - zona_de_lavanderia  1   0.01286 0.75568 -3606.1
    ## - tipo_de_inmueble    2   0.03575 0.77858 -3591.7
    ## - elevadores          1   0.04097 0.78379 -3586.0
    ## - administracion      1   0.05355 0.79638 -3577.2
    ## - banos               1   0.06366 0.80649 -3570.3
    ## - garajes             1   0.08771 0.83053 -3554.1
    ## - log(area)           1   0.15032 0.89315 -3514.0
    ## - estrato             4   0.51207 1.25490 -3332.7
    ## 
    ## Step:  AIC=-3616.42
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion + 
    ##     elevadores + tipo_de_inmueble + zona_de_lavanderia + porteria + 
    ##     antiguedad
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## + deposito            1   0.00520 0.73112 -3618.3
    ## <none>                            0.73632 -3616.4
    ## + habitaciones        1   0.00174 0.73458 -3615.7
    ## + area                1   0.00076 0.73555 -3615.0
    ## + remodelado          1   0.00003 0.73629 -3614.4
    ## + gas                 1   0.00003 0.73629 -3614.4
    ## + parqueadero         1   0.00002 0.73629 -3614.4
    ## - antiguedad          1   0.00651 0.74283 -3613.6
    ## - porteria            1   0.00865 0.74497 -3612.0
    ## - zona_de_lavanderia  1   0.01204 0.74836 -3609.5
    ## - elevadores          1   0.02080 0.75712 -3603.1
    ## - tipo_de_inmueble    2   0.03889 0.77521 -3592.1
    ## - administracion      1   0.05518 0.79150 -3578.6
    ## - banos               1   0.06040 0.79672 -3575.0
    ## - garajes             1   0.08598 0.82230 -3557.6
    ## - log(area)           1   0.15678 0.89310 -3512.1
    ## - estrato             4   0.50803 1.24435 -3335.3
    ## 
    ## Step:  AIC=-3618.33
    ## log(precio) ~ log(area) + estrato + garajes + banos + administracion + 
    ##     elevadores + tipo_de_inmueble + zona_de_lavanderia + porteria + 
    ##     antiguedad + deposito
    ## 
    ##                      Df Sum of Sq     RSS     AIC
    ## <none>                            0.73112 -3618.3
    ## + habitaciones        1   0.00159 0.72953 -3617.5
    ## + area                1   0.00052 0.73059 -3616.7
    ## - deposito            1   0.00520 0.73632 -3616.4
    ## + parqueadero         1   0.00012 0.73100 -3616.4
    ## + gas                 1   0.00004 0.73107 -3616.4
    ## + remodelado          1   0.00002 0.73110 -3616.3
    ## - antiguedad          1   0.00536 0.73647 -3616.3
    ## - porteria            1   0.00862 0.73974 -3613.9
    ## - zona_de_lavanderia  1   0.01130 0.74242 -3611.9
    ## - elevadores          1   0.01983 0.75094 -3605.6
    ## - tipo_de_inmueble    2   0.03887 0.76998 -3593.8
    ## - administracion      1   0.05302 0.78414 -3581.8
    ## - banos               1   0.06060 0.79172 -3576.5
    ## - garajes             1   0.07603 0.80714 -3565.8
    ## - log(area)           1   0.15302 0.88414 -3515.6
    ## - estrato             4   0.49920 1.23032 -3339.6

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ log(area) + estrato + garajes + banos + 
    ##     administracion + elevadores + tipo_de_inmueble + zona_de_lavanderia + 
    ##     porteria + antiguedad + deposito, data = propiedades, weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.110717 -0.026087  0.000273  0.025729  0.135210 
    ## 
    ## Coefficients:
    ##                                             Estimate Std. Error t value
    ## (Intercept)                                1.698e+01  1.452e-01 116.937
    ## log(area)                                  4.300e-01  4.063e-02  10.582
    ## estrato3                                   2.549e-01  1.708e-02  14.926
    ## estrato4                                   4.729e-01  2.591e-02  18.250
    ## estrato5                                   4.692e-01  3.866e-02  12.138
    ## estrato6                                   5.015e-01  4.901e-02  10.232
    ## garajes                                    1.373e-01  1.841e-02   7.459
    ## banos                                      1.036e-01  1.556e-02   6.659
    ## administracion                             3.828e-07  6.145e-08   6.229
    ## elevadores                                 4.058e-02  1.065e-02   3.809
    ## tipo_de_inmuebleCasa                       2.717e-01  5.798e-02   4.686
    ## tipo_de_inmueblecasa con conjunto cerrado  8.710e-02  3.145e-02   2.770
    ## zona_de_lavanderiaSi                       6.503e-02  2.261e-02   2.876
    ## porteriaSi                                -6.443e-02  2.565e-02  -2.512
    ## antiguedad                                -1.652e-03  8.342e-04  -1.980
    ## depositoSi                                 4.015e-02  2.058e-02   1.951
    ##                                           Pr(>|t|)    
    ## (Intercept)                                < 2e-16 ***
    ## log(area)                                  < 2e-16 ***
    ## estrato3                                   < 2e-16 ***
    ## estrato4                                   < 2e-16 ***
    ## estrato5                                   < 2e-16 ***
    ## estrato6                                   < 2e-16 ***
    ## garajes                                   3.55e-13 ***
    ## banos                                     6.84e-11 ***
    ## administracion                            9.51e-10 ***
    ## elevadores                                0.000156 ***
    ## tipo_de_inmuebleCasa                      3.54e-06 ***
    ## tipo_de_inmueblecasa con conjunto cerrado 0.005803 ** 
    ## zona_de_lavanderiaSi                      0.004189 ** 
    ## porteriaSi                                0.012313 *  
    ## antiguedad                                0.048218 *  
    ## depositoSi                                0.051583 .  
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.03697 on 535 degrees of freedom
    ## Multiple R-squared:  0.909,  Adjusted R-squared:  0.9064 
    ## F-statistic: 356.1 on 15 and 535 DF,  p-value: < 2.2e-16

Este nuevo modelo tiene 11 predictores, aunque depositoSI tiene pvalue
\>0.05

este modelo es interesante, mejora el ajuste en aproximadamente 0.01,
sin embargo , con esta nueva combinación de variables el modelo incumple
un supuesto.

    ## 
    ##  RESET test
    ## 
    ## data:  m_step_aic
    ## RESET = 6.4936, df1 = 2, df2 = 533, p-value = 0.001636

Se rechaza la hipótesis nula con alpha=0.05,

Este modelo será descartado y se continuará con el actual, nótese que
AIC_both=-3618.33 y AIC_actual= -3573, afortunadamente la diferencia no
es demasiada

## 6.5 *Validación y pronósticos del modelo.*

Para evitar data-leakage, se partira desde 0: Se leerán los datos de
nuevo, se partiran en conjuntos de entrenamiento y pruebas, se
realizarán las transformaciones necesarias y se procederá al
entrenamiento y la validación del modelo

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + log(area) + banos + garajes + 
    ##     elevadores + esCasa + zona_de_lavanderia, data = train, weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.108925 -0.024720 -0.001721  0.026606  0.142174 
    ## 
    ## Coefficients:
    ##                      Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept)          16.84658    0.15755 106.927  < 2e-16 ***
    ## estrato3              0.26217    0.01908  13.739  < 2e-16 ***
    ## estrato4              0.50824    0.02785  18.250  < 2e-16 ***
    ## estrato5              0.53086    0.04123  12.874  < 2e-16 ***
    ## estrato6              0.65189    0.05382  12.113  < 2e-16 ***
    ## log(area)             0.45036    0.04368  10.309  < 2e-16 ***
    ## banos                 0.11186    0.01774   6.305 7.15e-10 ***
    ## garajes               0.18558    0.02094   8.864  < 2e-16 ***
    ## elevadores            0.04940    0.01076   4.591 5.79e-06 ***
    ## esCasaSi              0.22450    0.05937   3.781 0.000178 ***
    ## zona_de_lavanderiaSi  0.07463    0.02703   2.760 0.006019 ** 
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.0386 on 430 degrees of freedom
    ## Multiple R-squared:  0.8977, Adjusted R-squared:  0.8953 
    ## F-statistic: 377.3 on 10 and 430 DF,  p-value: < 2.2e-16

    ##                       MAE                   MSE          RMSE     R2    MAPE
    ## Train_Log          0.1228                0.0234        0.1528 0.9050  0.6384
    ## Test_Log           0.1275                0.0265        0.1627 0.9051  0.6585
    ## Train_Nivel 32351730.1140 2434819798897958.5000 49343893.2280 0.8821 12.3599
    ## Test_Nivel  38475231.5748 3838928341713050.5000 61959086.0303 0.8616 12.8726

Las metricas del modelo fueron similares en conjuntos de entrenamiento y
prueba tanto en log-log como en level-level.

No existe evidencia de sub o sobre ajuste. El modelo tiene métricas
aceptables para la predicción de precios. Se equivoca en promedio un 12%
para predecir el precio.

# 7 *Interpretacion final*

Finalmente se obtuvo que las variables predictoras logran explicar un
89.95% de la varianza del precio, la formula. $$
w_i = \frac{1}{\left[\log(\text{area}_i)\right]^2}
$$

$$
\begin{aligned}
\log(\text{precio}_i) =\;& 16.6877 
+ 0.2606\,\text{estrato3}_i 
+ 0.5012\,\text{estrato4}_i 
+ 0.5503\,\text{estrato5}_i \\
&+ 0.6120\,\text{estrato6}_i 
+ 0.4933\,\log(\text{area}_i) 
+ 0.1071\,\text{banos}_i \\
&+ 0.1680\,\text{garajes}_i 
+ 0.0547\,\text{elevadores}_i 
+ 0.2344\,\text{esCasaSi}_i \\
&+ 0.0568\,\text{zona\_de\_lavanderiaSi}_i 
+ \varepsilon_i
\end{aligned}
$$ Nos permite dar una buena predicción del precio de un inmueble.

De esta forma se obtiene que:

- $(e^{0.2606} - 1) \times 100 = 29.8\%$. Una vivienda en estrato 3
  tiene un precio, en promedio, $29.8\%$ mayor que una vivienda en
  estrato (1 o 2).

- $(e^{0.5012} - 1) \times 100 = 65.0\%$. Una vivienda en estrato 4
  tiene un precio, en promedio, $65.0\%$ mayor que una vivienda en
  estrato (1 o 2)).

- $(e^{0.5503} - 1) \times 100 = 73.4\%$. Una vivienda en estrato 5
  tiene un precio, en promedio, $73.4\%$ mayor que una vivienda en
  estrato (1 o 2).

- $(e^{0.6120} - 1) \times 100 = 84.4\%$. Una vivienda en estrato 6
  tiene un precio, en promedio, $84.4\%$ mayor que una vivienda en
  estrato (1 o 2).

- Un aumento del 1% en el area se asocia con un aumento de 49% en el
  precio.

- Un baño adicional genera un aumento de 10.7% el precio.

- Un garaje adicional genera un aumento de 16.8% en el precio.

- Un elevador adicional genera un aumento de 5.4% en el precio.

- El hecho de que un inmueble sea casa aumento genera un aumento de
  23.4% en el precio.

- El hecho de que un inmueble tenga lavandería aumento genera un aumento
  de 23.4% en el precio.

*Como se puede apreciar, los B´s de estrato en la interpretación no son
los mismos que salen en el modelo, esto porque al realizar una consulta
, se descubrió que la forma correcta de interpretarlos era usando una
corrección de la forma (e^{B} - 1). La principal referencia puede verse
aquí: *

\*\_ Halvorsen, R. & Palmquist, R. (1980). The Interpretation of Dummy
Variables in Semilogarithmic Equations. American Economic Review, 70(3),
474–475. \_\*

<https://scispace.com/pdf/the-interpretation-of-dummy-variables-in-semilogarithmic-54qeaggyyn.pdf>

## 7.1 Rango

El rango de predicción es en el cual el modelo puede dar predicciones
acertadas con la confianza estadísitica obtenida , este es

    ## [1]   85000000 1530000000

Suficiente para dar un precio a bastantes inmuebles, pero no a todos los
de bogotá.

# 8 *Conclusiones y hallazgos relevantes*

- Todos los modelos tuvieron R2 alto (mayor a 0.85)

- Antes de pensar en hacer transformaciones, todos los modelos fallaban
  la prueba de linealidad, lo que da a lugar a pensar de que sí existen
  relaciones no lineales necesarias para el modelo.

- Ajustes para validar un supuesto pueden dañar otros supuestos.

- Puede ser común encontrar segmentaciones ocultas en Precio con
  respecto a otras variables en conjuntos de datos inmobiliarios

- La inclusión de variables en un formato incorrecto puede cambiart
  todo, en este caso estrato fue previamente tratada como entera, de
  esta forma se encontraron dificultades an la prueba de los supuestos.
  Al incluirla como factor (categorica) este problema fue solucionado
  facilmente.

- Las observaciones que presentan apalancamiento no necesariamente son
  influyentes; de las 50 observaciones con apalancamiento, solo 14 se
  determinaron influyentes.

# 9 *Recomendaciones futuras*

- Obtener mas datos: mayor cantidad de datos hubiese podido crear
  significancia para otras variables, incluso pudiendo permitir que
  todos los supuestos se validen mas facilmente.

- Acotar la región de predicción: En el conjunto de datos existe
  concentración de valores en algunas variables, en particular en
  precio:

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-76-1.png)<!-- -->

- Buscar una mejora en el modelo final: Aunque modelo_wls pasa todas la
  prueba de linealidad, es natural pensar en interacciones, por ejemplo,
  entre area y estrato, e incluso la inclusión de ‘administración’ en
  alguna potencia.

# 10 Anexos

## 10.1 1. Modelos calculados con estrato numérico:

Nota: todo lo que está en esta sección no se considera parte del
análisis, por lo tanto las conclusiones presentees en esta sección no
deben ser tomadas como verdaderas.

Durante el desarrollo del primer informe se habia trabajado con estrato
como variable numérica, sin embargo durante la segunda entrega esto
cambia para ser tratada como variable categórica, esto permitio que los
supuestos de el primer modelo con pesos se cumplieran, es por ello que
aquí se adjuntan los modelos que se habian intentado DESPUÉS del modelo
con pesos cuando se usaba estrato como variable numerica:

### 10.1.1 `Modelo con pesos y combinaciones`

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato + (log(area) * estrato) + 
    ##     log(area) + I(log(area)^2) + banos + garajes + elevadores + 
    ##     esCasa + zona_de_lavanderia + I(banos/log(area)) + I(garajes/log(area)), 
    ##     data = propiedades, weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.107268 -0.023379 -0.001615  0.022649  0.147424 
    ## 
    ## Coefficients:
    ##                       Estimate Std. Error t value             Pr(>|t|)    
    ## (Intercept)          23.093953   1.235026  18.699 < 0.0000000000000002 ***
    ## estrato               1.043317   0.115052   9.068 < 0.0000000000000002 ***
    ## log(area)            -3.486611   0.641735  -5.433    0.000000083976416 ***
    ## I(log(area)^2)        0.584957   0.084862   6.893    0.000000000015314 ***
    ## banos                -0.326825   0.215258  -1.518               0.1295    
    ## garajes              -0.280047   0.281147  -0.996               0.3197    
    ## elevadores            0.056576   0.009395   6.022    0.000000003193553 ***
    ## esCasaSi              0.142674   0.057863   2.466               0.0140 *  
    ## zona_de_lavanderiaSi  0.030885   0.022860   1.351               0.1772    
    ## I(banos/log(area))    1.773847   0.875049   2.027               0.0431 *  
    ## I(garajes/log(area))  1.864665   1.168187   1.596               0.1110    
    ## estrato:log(area)    -0.213839   0.028032  -7.628    0.000000000000108 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.0375 on 539 degrees of freedom
    ## Multiple R-squared:  0.9056, Adjusted R-squared:  0.9037 
    ## F-statistic: 470.2 on 11 and 539 DF,  p-value: < 0.00000000000000022

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-78-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-78-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-78-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-78-4.png)<!-- -->

#### 10.1.1.1 `Comprobación de suspuestos de modelo con pesos y combinacion de variables`

<center>

#### 10.1.1.2 \* 1. Prueba de linealidad Y vs X - Test de Ramsey \*

</center>

$$
\begin{aligned}
H_0 &: \text{El modelo está correctamente especificado (no hay variables omitidas ni no linealidad).} \\
H_1 &: \text{El modelo está mal especificado (existen variables omitidas o no linealidad).}
\end{aligned}
$$

    ## 
    ##  RESET test
    ## 
    ## data:  modelo_wls2
    ## RESET = 3.6983, df1 = 2, df2 = 537, p-value = 0.0254

No se rechaza la hipótesis nula con alpha=0.05,

<center>

#### 10.1.1.3 \* 2. Prueba de Breusch Pagan - Homocedasticidad \*

</center>

$$
\begin{aligned}
H_0 &: \operatorname{Var}(\varepsilon_i) = \sigma^2 \quad \text{(los errores tienen varianza constante)} \\
H_1 &: \operatorname{Var}(\varepsilon_i) \neq \sigma^2 \quad \text{(existe heterocedasticidad)}
\end{aligned}
$$

    ## 
    ##  studentized Breusch-Pagan test
    ## 
    ## data:  modelo_wls2
    ## BP = 11.129, df = 11, p-value = 0.4325

NO se rechaza la hipótesis nula con alpha=0.05,

<center>

#### 10.1.1.4 \* 3. Prueba de autocorrelacion de los errores - Durbin Watson \*

</center>

$$
\begin{aligned}
H_0 &: \rho = 0 \quad \text{(no hay autocorrelación de los errores)} \\
H_1 &: \rho \neq 0 \quad \text{(los errores están correlacionados)}
\end{aligned}
$$

    ##  lag Autocorrelation D-W Statistic p-value
    ##    1       -0.087647      2.173546    0.04
    ##  Alternative hypothesis: rho != 0

NO se rechaza la hipotesis nula de que los errores son dependientes
entre sí, se puede decir que

<center>

#### 10.1.1.5 \* 4. Prueba de normalidad de los errores- Shapiro \*

</center>

$$
\begin{aligned}
H_0 &: \varepsilon_i \sim N(0, \sigma^2) \quad \text{(los residuos son normalmente distribuidos)} \\
H_1 &: \varepsilon_i \not\sim N(0, \sigma^2) \quad \text{(los residuos no son normales)}
\end{aligned}
$$

    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  modelo_wls2$residuals
    ## W = 0.99466, p-value = 0.05177

NO se rechaza la hipotesis nula con un nivel de significancia de 0.05 de
que el vector dado(residuales) tiene una distribución normal.

<center>

#### 10.1.1.6 *VIF - verificacion de inflación de varianza por colinealidad*

</center>

    ##              estrato            log(area)       I(log(area)^2) 
    ##           343.655506           840.197855           996.938848 
    ##                banos              garajes           elevadores 
    ##           437.992900           670.326891             1.208587 
    ##               esCasa   zona_de_lavanderia   I(banos/log(area)) 
    ##             1.096523             1.031670           334.097418 
    ## I(garajes/log(area))    estrato:log(area) 
    ##           615.387077           415.183219

Varios VIF sobrepasan 10 por mucho, Aqui se llegó a un modelo que cumple
los cuatro supuestos clásicos: - Linealidad X vs Y - Homocedasticidad -
Errores independientes - Normalidad de los errores A pesar de lo
anterior, los valores vif se dispararon porque se hicieron combinaciones
entre variables, se intentará hacer un modelo más donde se pueda reducir
ese VIF.

Para ello, se deberá evitar las combinaciones lineales, entonces se hará
que algunos términos usen el area normal, pero otros usarán el logaritmo
del area ,centrado por su media. Entonces así no habrá colinealidades
tan fuertes .

### 10.1.2 Segundo Modelo con pesos y combinaciones (con centrado de log(area))

    ## 
    ## Call:
    ## lm(formula = log(precio) ~ estrato * log_area_c + I(log_area_c^2) + 
    ##     elevadores + esCasa + I(banos/area) + I(garajes/area), data = propiedades, 
    ##     weights = 1/log(area)^2)
    ## 
    ## Weighted Residuals:
    ##       Min        1Q    Median        3Q       Max 
    ## -0.109587 -0.023344 -0.001817  0.022890  0.147488 
    ## 
    ## Coefficients:
    ##                     Estimate Std. Error t value             Pr(>|t|)    
    ## (Intercept)        18.572548   0.028728 646.496 < 0.0000000000000002 ***
    ## estrato             0.177757   0.009464  18.782 < 0.0000000000000002 ***
    ## log_area_c          1.255955   0.067846  18.512 < 0.0000000000000002 ***
    ## I(log_area_c^2)     0.552474   0.058813   9.394 < 0.0000000000000002 ***
    ## elevadores          0.058505   0.009343   6.262 0.000000000775994627 ***
    ## esCasaSi            0.146267   0.057964   2.523               0.0119 *  
    ## I(banos/area)       6.241379   0.873965   7.141 0.000000000002987480 ***
    ## I(garajes/area)    10.335353   1.092591   9.459 < 0.0000000000000002 ***
    ## estrato:log_area_c -0.205959   0.024704  -8.337 0.000000000000000631 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 0.03757 on 542 degrees of freedom
    ## Multiple R-squared:  0.9047, Adjusted R-squared:  0.9033 
    ## F-statistic: 643.2 on 8 and 542 DF,  p-value: < 0.00000000000000022

![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-84-1.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-84-2.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-84-3.png)<!-- -->![](Segundo-informe_Julian-Gaitan_ANALISIS-DE-REGRESION_files/figure-gfm/unnamed-chunk-84-4.png)<!-- -->

#### 10.1.2.1 `Comprobación de suspuestos del segundo modelo con pesos y combinacion de variables`

<center>

#### 10.1.2.2 \* 1. Prueba de linealidad Y vs X - Test de Ramsey \*

</center>

$$
\begin{aligned}
H_0 &: \text{El modelo está correctamente especificado (no hay variables omitidas ni no linealidad).} \\
H_1 &: \text{El modelo está mal especificado (existen variables omitidas o no linealidad).}
\end{aligned}
$$

    ## 
    ##  RESET test
    ## 
    ## data:  modelo_final
    ## RESET = 3.6072, df1 = 2, df2 = 540, p-value = 0.02778

No se rechaza la hipótesis nula con alpha=0.05,

<center>

#### 10.1.2.3 \* 2. Prueba de Breusch Pagan - Homocedasticidad \*

</center>

$$
\begin{aligned}
H_0 &: \operatorname{Var}(\varepsilon_i) = \sigma^2 \quad \text{(los errores tienen varianza constante)} \\
H_1 &: \operatorname{Var}(\varepsilon_i) \neq \sigma^2 \quad \text{(existe heterocedasticidad)}
\end{aligned}
$$

    ## 
    ##  studentized Breusch-Pagan test
    ## 
    ## data:  modelo_final
    ## BP = 10.716, df = 8, p-value = 0.2183

NO se rechaza la hipótesis nula con alpha=0.05,

<center>

#### 10.1.2.4 \* 3. Prueba de autocorrelacion de los errores - Durbin Watson \*

</center>

$$
\begin{aligned}
H_0 &: \rho = 0 \quad \text{(no hay autocorrelación de los errores)} \\
H_1 &: \rho \neq 0 \quad \text{(los errores están correlacionados)}
\end{aligned}
$$

    ##  lag Autocorrelation D-W Statistic p-value
    ##    1     -0.08464552      2.167524   0.048
    ##  Alternative hypothesis: rho != 0

NO se rechaza la hipotesis nula de que los errores son dependientes
entre sí, se puede decir que

<center>

\####\* 4. Prueba de normalidad de los errores- Shapiro \*

</center>

$$
\begin{aligned}
H_0 &: \varepsilon_i \sim N(0, \sigma^2) \quad \text{(los residuos son normalmente distribuidos)} \\
H_1 &: \varepsilon_i \not\sim N(0, \sigma^2) \quad \text{(los residuos no son normales)}
\end{aligned}
$$

    ## 
    ##  Shapiro-Wilk normality test
    ## 
    ## data:  modelo_final$residuals
    ## W = 0.99375, p-value = 0.02251

Se rechaza la hipotesis nula con un nivel de significancia de 0.05 de
que el vector dado(residuales) tiene una distribución normal. ,

<center>

#### 10.1.2.5 \* 5. Prueba de Varianza no constante\*

</center>

    ## Non-constant Variance Score Test 
    ## Variance formula: ~ fitted.values 
    ## Chisquare = 1.313921, Df = 1, p = 0.25169

<center>

#### 10.1.2.6 *VIF - verificacion de inflación de varianza por colinealidad*

</center>

    ##            estrato         log_area_c    I(log_area_c^2)         elevadores 
    ##           2.315822           9.352321           1.467710           1.190376 
    ##             esCasa      I(banos/area)    I(garajes/area) estrato:log_area_c 
    ##           1.095779           1.121591           1.982028           9.554411

Se logró el objetivo en este modelo: reducir el VIF, sin embargo se
desajustó la normalidad de los errores, el valor p cambia a 0.03, lo que
rompe el supuesto de normalidad por muy poco (Qqplot parece normal
visualmente)

En este caso, se preferirá este modelo final, es el mejor modelo hallado
porque no tiene de colinealidad y se cumplen todos los supuestos,
excepto el de normalidad con un nivel de si+gnificancia de 0.05 (si se
usara un alpha de 0.01 - 0.03 se podria no rechazar h0, indicando
normalidad)

\`\`\`
