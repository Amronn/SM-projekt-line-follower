# SM-projekt-line-follower
Elementy składające się na pojazd:
- dwa silniki dc 3-6V 
- sterownik L298n
- płytka stm32F756ZG
- czujniki CNY70
- obudowa złożona z kawałka sklejki, dwóch kółek i jednego kółka skrętnego.
- powerbank -zasilanie układu

W celu odczytania pozycji pojazdu względem linii, wyjścia z czujników CNY70 są połączone kolejno do wejść analogowych do pinów:
| Nr Pinu | Pin na STM32 | Pin na Arduino |
|---------|-----------|-------------|
|   1    |   PA_3    |      A0     |
|   2    |   PC_0    |      A1     |
|   3    |   PC_3    |      A2     |
|   4    |   PF_3    |      A3     |
|   5    |   PF_5    |      A4     |

Do sterowania silników został użyty sterownik L298n. Silniki są sterowane za pomocą PWM z TIM1.
