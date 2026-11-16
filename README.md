
# O-MOUSE — Óculos para tetraplígicos (Controle total do Computador)

Desenvolvi o **O-MOUSE**, um dispositivo de tecnologia assistiva que permite controlar o cursor do computador utilizando movimentos da cabeça e piscadas dos olhos, sem a necessidade de utilizar as mãos. Com ele é possível controlar o conputador como um mouse convencional, simulando todas as suas funçoes de botao direito e esquerdo e scroll, cliques simples, duplos, três cliques simula botao direito e etc. Para teclado e digitação indicamos o uso do teclado virtual, 

O projeto tem como principal objetivo proporcionar **acessibilidade, autonomia e inclusão digital**, especialmente para pessoas com limitações motoras severas, como tetraplegia.

| Tutoriais/Título | Descrição/Link Medium | Links/Vídeos YouTube | Links/Códigos fonte |
| --- | --- | --- | --- |
| O-MOUSE — Óculos Inteligentes Assistivos | Em desenvolvimento | Em breve | Em breve |

<br>

## O Projeto O-MOUSE

O **O-MOUSE** é um sistema eletrônico embarcado desenvolvido para transformar movimentos naturais da cabeça e piscadas dos olhos em comandos de um mouse convencional.

O dispositivo utiliza o microcontrolador **Seeed Studio XIAO nRF52840 Sense**, equipado com comunicação Bluetooth Low Energy (BLE), em conjunto com sensores de movimento e proximidade.

A proposta é oferecer uma alternativa aos dispositivos tradicionais de entrada, permitindo que pessoas com mobilidade reduzida utilizem computadores com maior independência.

<br>

## Tecnologias e Componentes Utilizados

- **XIAO nRF52840 Sense:** microcontrolador ARM Cortex-M4F com Bluetooth Low Energy (BLE).
- **LSM6DS3:** sensor de movimento de 6 eixos, com acelerômetro e giroscópio.
- **APDS9960:** sensor óptico utilizado para detectar piscadas por meio de variações de proximidade.
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

### 5. Gerenciamento de Energia

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

