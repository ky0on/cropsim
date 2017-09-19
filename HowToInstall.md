# How to Install

## Install
```
library(devtools)
install_github('ky0on/cropsim', subdir='pkg/oldweather')
install_github('ky0on/cropsim', subdir='pkg/cropsim')
```

## Test
```
library(cropsim)
library(oldweather)
wth <- getWthFile(system.file("weather/daily_weather_28368.nasa", package = "cropsim"))
cv <- simriwCultivar('Nipponbare')
sim <- simriw(wth, cv, startday='2000-05-15')
plot(sim)
```