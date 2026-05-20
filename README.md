# Estudio fase IV de Velmyra contra VRS-X

Este repositorio contiene un entorno reproducible de R para el trabajo práctico de la materia **Inferencia Bayesiana** de la Maestría en Explotación de Datos y Descubrimiento de Conocimiento de la UBA.

## Requisitos

- R 4.x
- RStudio
- RTools

En Windows, verificar RTools con:

```r
install.packages("pkgbuild")
pkgbuild::check_build_tools(debug = TRUE)
```

### Replicar el entorno

Clonar el repositorio y abrir el proyecto en RStudio. Luego correr:

```r
install.packages("renv")
renv::restore()
```

Esto instala las versiones de paquetes registradas en renv.lock.

### CmdStan

`renv` instala el paquete `cmdstanr`, pero no instala CmdStan automáticamente. Verificar con:

```r
library(cmdstanr)
cmdstanr::check_cmdstan_toolchain()
cmdstanr::cmdstan_path()
```

Si CmdStan no está instalado:
```r
cmdstanr::install_cmdstan(cores = 2)
```

### Paquetes principales

El entorno incluye paquetes generales y bayesianos usados en la materia, entre ellos:

```r
library(tidyverse)
library(tidymodels)
library(rstan)
library(brms)
library(bayesplot)
library(tidybayes)
library(cmdstanr)
library(rethinking)
library(ibUBA)
```
