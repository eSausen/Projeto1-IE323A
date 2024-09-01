# Projeto 1 - Explorando a Química e a Matemática com a BitDogLab - IE323A

## Introdução
  Este projeto desenvolve um sistema embarcado educativo que utiliza um Display OLED e uma Matriz RGB da BitDogLab para facilitar o ensino de matemática e química. O Display OLED exibe formas geométricas e fórmulas matemáticas, enquanto a Matriz RGB simula átomos e o compartilhamento de elétrons. A interface é interativa, permitindo a navegação entre tópicos através de botões, proporcionando uma experiência de aprendizado dinâmica e personalizada.

## Objetivos
1. **Uso do Display OLED:** Exibir formas geométricas e fórmulas matemáticas para melhorar a compreensão de conceitos.

2. **Simulação Química com Matriz RGB:** Representar átomos e camadas de valência, facilitando o entendimento de química.

3. **Botões de Entrada:** Permitir navegação interativa entre modos e tópicos.

4. **Interface Intuitiva:** Focar no aprendizado enquanto o sistema gerencia a complexidade técnica.

5. **Apoio ao Ensino Cooperativo:** Promover colaboração entre estudantes e professores, facilitando o aprendizado coletivo.

   Este projeto está alinhado com as habilidades específicas da BNCC, como a análise crítica de programas (EF07CO02) e a construção de soluções computacionais em diferentes áreas do conhecimento (EF07CO03). Mesmo que o foco não seja a programação direta pelos alunos, o sistema embarcado desenvolvido oferece uma oportunidade prática para exercitar essas habilidades através da interação com as representações visuais presentes no projeto.

## Teoria e Aplicação no Ensino de Química e Matemática

**Ensino de Química - Regra do Octeto**

  O projeto utiliza a Matriz RGB para simular átomos e suas camadas de valência, ilustrando conceitos fundamentais como a Regra do Octeto. Elementos como Hidrogênio, Hélio, Carbono e Oxigênio são visualmente representados, mostrando como os átomos compartilham ou recebem elétrons para atingir a estabilidade.

    Hidrogênio (H): Mostra a necessidade de uma ligação química para estabilizar seu único elétron.
    Hélio (He): Demonstra a estabilidade natural com dois elétrons, sem necessidade de ligação.
    Carbono (C): Exibe a necessidade de quatro ligações covalentes para estabilidade.
    Oxigênio (O): Mostra a necessidade de compartilhar dois elétrons para estabilização.

  Os alunos podem interagir com o sistema, selecionando elementos e visualizando suas camadas de valência em tempo real, reforçando o entendimento das ligações químicas.
Ensino de Matemática - Geometria Plana Básica

**Ensino de Matemática**

  O sistema embarcado utiliza o Display OLED para desenhar e interagir com figuras geométricas planas, como quadrados, retângulos, triângulos e círculos, aplicando fórmulas para cálculo de áreas.

    Quadrado: Representa todos os lados iguais, aplicando a fórmula Área = $L^2$. Onde "L" representa o Lado do quadrado
    Retângulo: Calcula a área como Área = $b x h$. Sendo "b" equivalente a base e "h" a altura do retângulo

  Os alunos podem exercitar os calculos de geometria das figuras, com exemplos pré-carregados na memória do raspberry pi pico embarcado na BitDogLab, usando diretamente no display, o que facilita a compreensão prática dos conceitos matemáticos.

## Funcionamento do Software na BitDogLab e Explicação dos Códigos Python

  Os arquivos base para embarcar na BitDOgLab e aplicação das atividades de química e matemática, os quais estão incluídos na pasta main deste projeto, são respectivamente "rgb-matrix-chemestry.py" e "display-oled-geometry.py".

  Estes códigos em linguagem Python estão organizados da seguinte maneira:
1. **Definição das Classes e Parâmetros Iniciais**:
  Inicialmente, definimos as classes a serem utilizadas no código, como Pin, SoftI2C e SSD1306_I2C.
  Estabelecemos os parâmetros para o display OLED e a matriz RGB, como por exemplo: oled = SSD1306_I2C(128, 64, i2c) e np = neopixel.NeoPixel(machine.Pin(7), 25).

3. **Configuração da Matriz RGB**:
  Definimos a intensidade, as cores e o padrão de cores desejado para a matriz RGB.
  Criamos uma função para a matriz de LED e para passar os valores configurados anteriormente.

4. **Definição das Funções do Projeto**:
  Desenvolvemos as funções que determinam o que será exibido no display de LED e na matriz RGB.
  Estabelecemos as informações que queríamos que fossem mostradas.

5. **Implementação da Lógica de Controle**:
  Criamos a função switch_case_dicionario(value) para definir quais funções serão chamadas com base no valor recebido.
  Utilizamos return cases.get(value, case0)() para buscar e executar as funções descritas anteriormente.

6. **Controle por Botão e Laço de Repetição**:
  Definimos a variável count e utilizamos um laço while para controlar o botão e selecionar as funções de acordo com o valor de count.

Para mais detalhes sobre o funcionamento do arquivos e como utilizá-lo, consulte os próprios códigos fonte que possuem comentários e estão disponíveis neste repositório.

**Incluir exemplo explicado de depuração dos códigos na BitDogLab com imagens da matriz RGB com algum átomo e do display oled exibindo uma poligono e sua área calculada**
