# KHSLiveUSB
Neuro Reticulum LiveUSB image 

```php
  _  ___    _  _____ 
 | |/ / |  | |/ ____|
 | ' /| |__| | (___  
 |  < |  __  |\___ \ 
 | . \| |  | |____) |
 | |\_\_|  |_|_____/ 
 | (_)               
 | |___   _____      
 | | \ \ / / _ \     
 | | |\ V /  __/     
 |_|_| \_/ \___|     
```
Образ 16Gb KHSLiveUSB основан на Debian 13 Trixie
Для запуска легковесных моделей нейросетей и организации сетевых соединений Reticulum


В образ интегрированы следующие инструменты:
- llama.cpp 
- stable-diffusion.cpp (без моделей)
- whisper.cpp

Модели:
- DeepSeek-R1-0825-8B
- перевод whisper-large-turbo-q5_0
- medgemma-4B

Сетевые инструменты:
- Reticulum Network Stack (rns, nomadnet, sideband)

Мониторинг утилизации ресурсов:
- nmon
- lm-sensors
- psensor

Установка:
- Записать образ на usb флэшку с помощью dd или любых других инструментов, таких как Rufus или Balena Etcher
для оптимальной скорости работы лучше использовать флешки с хорошей скоростью чтения/записи стандарта 3.2

Download: HF link https://huggingface.co/cyberunit/KHSLiveUSB

### Образ протестирован на:

<details>

  <summary> <b>AMD Ryzen AI 9 365 (32Gb RAM)</b> </summary>
  
![image](images/amd_cfg.png)
Stable-Diffusion -> Flux (~9Gb)
![image](images/amd_sd.png)
10 min
</details>

<details>

  <summary> <b>Intel Core i5 9400F (8Gb RAM)</b> </summary>
  Illegal instruction решается пересборкой llama под новое железо
  запуск модели medgemma-4b-it-Q4_K_M (2.3Gb)

  ~9 t/s
![image](images/intel_cfg.png)
</details>
