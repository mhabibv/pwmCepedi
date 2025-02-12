# Controle de PWM para LED e Servomotor

Este projeto permite controlar um LED ou um servomotor utilizando PWM (Pulse Width Modulation) em um Raspberry Pi Pico.

## 📌 Requisitos
- Raspberry Pi Pico
- Ambiente de desenvolvimento configurado com o **Pico SDK**
- Um LED e/ou um Servomotor
- Cabo USB para alimentação e comunicação com o computador

## ⚙️ Configuração
### 1. Instale o Pico SDK
Se ainda não configurou o ambiente, siga a documentação oficial do Raspberry Pi para instalar o **Pico SDK** e o **CMake**.

### 2. Clone o repositório
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
```

### 3. Compile o código
```bash
mkdir build
cd build
cmake ..
ninja
```

### 4. Envie o programa para o Raspberry Pi Pico
1. Conecte o Raspberry Pi Pico no modo **BOOTSEL** (pressione o botão BOOTSEL ao conectar o cabo USB).
2. Copie o arquivo `pwmCepedi.uf2` gerado na pasta `build` para o drive montado do Pico.
3. O Raspberry Pi Pico reiniciará automaticamente e começará a executar o código.

## 🛠️ Funcionamento
O programa alterna automaticamente o pino de PWM entre um LED e um servomotor.

- Se a opção **USE_LED** estiver ativada, o PWM será usado para variar o brilho do LED.
- Caso contrário, o PWM controlará a posição do servomotor, movendo-o entre 0 e 180 graus de forma contínua.

## Link do vídeo mostrando funcionamento
https://youtu.be/kD-mT0NVuzk?feature=shared
