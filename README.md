
# O-MOUSE — Óculos para tetraplígicos (Controle total do Computador)

Desenvolvi o **O-MOUSE**, um dispositivo de tecnologia assistiva que permite controlar o cursor do computador utilizando movimentos da cabeça e piscadas dos olhos, sem a necessidade de utilizar as mãos. Com ele é possível controlar o conputador como um mouse convencional, simulando todas as suas funçoes de botao direito e esquerdo e scroll, cliques simples, duplos, três cliques simula botao direito e etc. Para teclado e digitação indicamos o uso do teclado virtual, 

O projeto tem como principal objetivo proporcionar **acessibilidade, autonomia e inclusão digital**, especialmente para pessoas com limitações motoras severas, como tetraplegia.

| Tutoriais/Título | Descrição/Link Medium | Links/Vídeos YouTube | Links/Códigos fonte |
| --- | --- | --- | --- |
| O-MOUSE — Óculos Inteligentes Assistivos | Em desenvolvimento |  [Vídeo do projeto](https://youtu.be/0Xy8QtoHRoY?si=2TRkzyhtgwCKuBoa) | Em breve |

<br>

## O Projeto O-MOUSE

O **O-MOUSE** é um sistema eletrônico embarcado desenvolvido para transformar movimentos naturais da cabeça e piscadas dos olhos em comandos de um mouse convencional.

O dispositivo utiliza o microcontrolador **ESP32 C3 SUPERMINI**, equipado com comunicação Bluetooth Low Energy (BLE), em conjunto com sensores de movimento e proximidade.

A proposta é oferecer uma alternativa aos dispositivos tradicionais de entrada, permitindo que pessoas com mobilidade reduzida utilizem computadores com maior independência.

<p align="center">
  <img src="https://github.com/user-attachments/assets/5da7ed36-7fd2-47ed-9842-878685e6d3ca" width="50%" />
</p>

Toda estrutura plastica e de metal do prótotipo foi desenvolvido de forma artesanal em formato de Headset, com auxilio de peças impressas em 3d.
<br>



<br>

## Tecnologias e Componentes Utilizados

- **ESP32 C3 SUPERMINI:** Wifi E Bluetooth Usb-c Risc-v.
- **LSM6DS3:** sensor de movimento de 6 eixos, com acelerômetro e giroscópio.
- **APDS9940:** sensor óptico utilizado para detectar variações de proximidade.
- **AO3407:** MOSFET utilizado no gerenciamento da alimentação do sensor óptico.
- **Bluetooth BLE HID:** protocolo de comunicação que permite ao dispositivo funcionar como mouse Bluetooth.
- **Bateria recarregável:** alimentação portátil para utilização sem cabos.
- **C/C++:** linguagem de programação utilizada no desenvolvimento do firmware.

<br>

## Funcionalidades Desenvolvidas

### 1. Controle do Cursor por Movimentos da Cabeça

O sensor **LSM6DS3** identifica movimentos da cabeça por meio do acelerômetro e giroscópio, permitindo converter essas informações em deslocamentos do cursor do computador.

O sistema utiliza algoritmos de processamento dos sensores para melhorar a precisão, a estabilidade e a suavidade dos movimentos.

### 2. Reconhecimento de Piscadas

O sensor óptico **APDS9960** é utilizado para identificar piscadas a partir das alterações de proximidade provocadas pelo fechamento dos olhos.

Essa tecnologia permite implementar comandos como:

- Clique esquerdo.
- Clique duplo.
- Clique direito.
- Arrastar e soltar.
- Ativação de funções especiais.

O reconhecimento considera a duração e a sequência das piscadas para diferenciar os comandos.

### 3. Comunicação Bluetooth BLE

O O-MOUSE utiliza comunicação **Bluetooth Low Energy (BLE HID)** para transmitir os comandos ao computador.

O dispositivo é reconhecido como um mouse Bluetooth compatível, dispensando o uso de receptores USB dedicados.

### 4. Calibração e Ajustes

O firmware permite implementar ajustes para adaptar o funcionamento do dispositivo às necessidades de cada usuário.

Entre os parâmetros de calibração estão:

- Sensibilidade dos movimentos horizontais e verticais.
- Zona morta (Deadzone).
- Suavização do movimento do cursor.
- Tempo de reconhecimento das piscadas.
- Ajuste dos limites de detecção do sensor óptico.
- Calibração da posição neutra da cabeça.



### 5. Software Web de Configuração e Calibração

Além do hardware e do firmware embarcado, desenvolvi um **software de configuração e calibração do O-MOUSE**, que funciona diretamente no navegador de internet, sem necessidade de instalação de aplicativos.

A interface utiliza a tecnologia **Web Bluetooth API** para estabelecer comunicação sem fio com o microcontrolador XIAO nRF52840 Sense, permitindo configurar e ajustar o funcionamento dos óculos em tempo real.

O software foi desenvolvido para facilitar a personalização do dispositivo de acordo com as necessidades e características motoras de cada usuário.

**Principais recursos do software:**

- **Conexão Bluetooth:** identificação e conexão com o O-MOUSE diretamente pelo navegador.
- **Monitoramento dos sensores:** visualização das informações de movimento e proximidade recebidas do dispositivo.
- **Calibração do giroscópio:** ajuste da posição neutra da cabeça para melhorar a precisão do cursor.
- **Sensibilidade do cursor:** configuração dos movimentos horizontais e verticais.
- **Zona morta (Deadzone):** ajuste para evitar deslocamentos involuntários do ponteiro.
- **Suavização dos movimentos:** configuração dos parâmetros utilizados para reduzir oscilações do cursor.
- **Calibração das piscadas:** ajuste dos limites de detecção do sensor óptico APDS9960.
- **Configuração dos comandos:** personalização dos parâmetros utilizados no reconhecimento das piscadas.
- **Armazenamento das configurações:** envio dos parâmetros ao microcontrolador para armazenamento na memória não volátil.

#### Tecnologias Utilizadas no Software

- **HTML5:** estrutura da interface de configuração.
- **CSS3:** estilização e organização visual.
- **JavaScript:** implementação das funcionalidades e dos controles.
- **Web Bluetooth API:** comunicação direta entre navegador e dispositivo.
- **Bluetooth Low Energy (BLE):** transmissão dos parâmetros e informações dos sensores.
- **GATT:** utilização de serviços e características BLE para troca de dados entre o software e o firmware.

#### Funcionamento

O usuário acessa a interface Web por um navegador compatível com Web Bluetooth, conecta o O-MOUSE e realiza os ajustes necessários.

As configurações são transmitidas ao microcontrolador por Bluetooth, permitindo calibrar o dispositivo sem a necessidade de reprogramar ou atualizar o firmware a cada alteração.

O sistema foi concebido para proporcionar uma experiência de configuração simples, acessível e personalizada, facilitando a utilização do O-MOUSE por pessoas com diferentes necessidades motoras.

**Diferencial do projeto:** o O-MOUSE combina hardware embarcado, firmware C/C++ e software Web de calibração, formando uma solução integrada de tecnologia assistiva.


<p align="center">
  <img src="https://github.com/user-attachments/assets/7dfb745d-ce33-49eb-b214-76942ffb8555" width="50%" />
  <img src="https://github.com/user-attachments/assets/62ea3087-e192-4205-b214-415ab849e9a2" width="50%" />
  <img src="https://github.com/user-attachments/assets/9b9215c5-0ea3-41b2-8d5e-de6fa2d4a007" width="50%" />
  <img src="https://github.com/user-attachments/assets/097e65c1-f66e-42da-a2e5-88e6e0b727ff" width="50%" />

</p>



### 6. Gerenciamento de Energia

O projeto também contempla técnicas de gerenciamento de energia para aumentar a autonomia da bateria.

Entre os recursos estudados e implementados estão:

- Controle da alimentação do sensor óptico utilizando MOSFET.
- Monitoramento da atividade dos sensores.
- Redução do consumo durante períodos de inatividade.
- Monitoramento da bateria.
- Controle de funcionamento dos periféricos.

<br>

## Desafios Técnicos do Desenvolvimento

Durante o desenvolvimento do O-MOUSE, foram realizados testes e ajustes envolvendo diferentes áreas da engenharia eletrônica e de software.

**Principais desafios técnicos:**

- Identificação precisa das piscadas utilizando o sensor APDS9960.
- Diferenciação entre piscadas voluntárias e involuntárias.
- Processamento dos movimentos da cabeça com o giroscópio.
- Redução de movimentos involuntários do cursor.
- Otimização da comunicação BLE HID.
- Redução do consumo energético.
- Integração dos componentes em um dispositivo compacto e vestível.
- Desenvolvimento de algoritmos para reconhecimento de gestos e comandos.

<br>

## Aplicações da Tecnologia Assistiva

O O-MOUSE foi idealizado para auxiliar principalmente pessoas com limitações motoras que dificultam a utilização de dispositivos convencionais.

Entre suas possíveis aplicações estão:

- Acesso a computadores por pessoas com tetraplegia.
- Navegação na internet sem utilização das mãos.
- Utilização de softwares educacionais.
- Comunicação digital assistiva.
- Operação de interfaces computacionais.
- Apoio à inclusão digital de pessoas com deficiência motora.

<br>

## Evolução do Projeto

O desenvolvimento do O-MOUSE envolve diferentes etapas de pesquisa, implementação e testes.

| Etapa | Descrição |
| --- | --- |
| 1 | Estudo e seleção do microcontrolador XIAO nRF52840 Sense. |
| 2 | Integração do sensor de movimento LSM6DS3. |
| 3 | Desenvolvimento do controle do cursor por movimentos da cabeça. |
| 4 | Integração do sensor óptico APDS9960. |
| 5 | Testes e calibração da detecção de piscadas. |
| 6 | Implementação da comunicação Bluetooth BLE HID. |
| 7 | Desenvolvimento dos comandos de clique utilizando piscadas. |
| 8 | Estudos para otimização do consumo energético. |
| 9 | Integração eletrônica em um dispositivo vestível compacto. |
| 10 | Aperfeiçoamento contínuo do firmware e da experiência de utilização. |

<br>

## Objetivo Social

Mais do que um projeto de eletrônica e programação, o **O-MOUSE** representa uma iniciativa de aplicação da tecnologia para melhorar a acessibilidade.

Seu desenvolvimento busca demonstrar que soluções baseadas em **microcontroladores, sensores inteligentes, comunicação sem fio e software embarcado** podem contribuir para proporcionar mais autonomia a pessoas com deficiência motora.

O projeto continua em desenvolvimento e aperfeiçoamento, com foco na precisão, conforto, eficiência energética e facilidade de utilização.

<br>

**Área de desenvolvimento:** Engenharia de Computação, Sistemas Embarcados, Eletrônica, Bluetooth BLE, Programação C/C++ e Tecnologia Assistiva.

**Status:** Protótipo em desenvolvimento e testes.

