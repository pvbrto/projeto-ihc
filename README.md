# Projeto de Interface Humano-Computador

Projeto apresentado ao Centro Universitário [FEI](https://portal.fei.edu.br/), como parte dos requisitos necessários para aprovação na disciplina de Interface Humano-Computador (CC8122) do curso de Ciencia da Computação, orientado pelo Prof. Dr. [Fagner de Assis Moura Pimentel](https://github.com/fagnerpimentel) e Prof. Dr. Plino Thomaz Aquino Junior.

Este projeto se baseia no Trabalho de Conclusão de Curso (TCC) entitulado **IDENTIFICAÇÃO E REIDENTIFICAÇÃO CONTÍNUA DE PESSOAS EM AMBIENTES DE TRÁFEGO INTENSO UTILIZANDO ALGORITMOS DE VISÃO COMPUTACIONAL** sob orientação do Professor **Prof. Dr. Ricardo de Carvalho Destro** e desenvolvido pelos seguintes alunos:

- Gianluca Mariano Sobreiro - 22.122.011-4
- Guilherme Fornagiero de Carvalho - 22.122.016-3
- Paulo Vinícius Bessa de Brito - 22.122.005-6
- Pedro Augusto Bento Rocha - 22.122.028-8
- Thiago Garcia Santana - 22.122.003-1

## Resumo


## Introdução

Sobre o produto ou serviço que seu grupo está desenvolvendo, responda:
O projeto consiste no desenvolvimento de um sistema distribuído de larga escala, focando na identificação e reidentificação contínua de pessoas em ambientes de tráfego intenso, com foco no Metrô de São Paulo e em sua necessidade de mapeamento de fluxos em suas estações. O sistema utiliza algoritmos de visão computacional e aprendizado de máquina para rastrear passageiros entre diferentes câmeras, mesmo em condições adversas como mudanças de iluminação, ângulos de filmagem e pequenas alterações na aparência. O objetivo principal é fornecer ao Metrô de São Paulo uma ferramenta capaz de monitorar o fluxo de passageiros, identificar indivíduos de forma contínua e precisa, e auxiliar na gestão operacional e segurança do transporte público. Além disso, focado na disciplina de Interface Humano-Computador, aumentamos o escopo do projeto, para trabalhar também com a análise dos dados capturados, e a geração de resultados a partir destes.

Usuário final: Companhia do Metropolitano de São Paulo (Metrô-SP) equipes de segurança e de gestão operacional do sistema metroviário.

Baseado em uma geração de base de dados diária/semanal do fluxo de pessoas que passam pelas estações do Metrô de São Paulo, e o envio/análise desses dados, podemos ter a otimização da alocação de recursos operacionais (trens, funcionários, segurança) pela diretoria do Metrô, focada em melhorar a experiência do usuário final (o passageiro). Além disso, o aumento da segurança, com possibilidade de detectar indivíduos específicos (como vendedores ambulantes ilegais) e um melhor mapeamento de rotas para os passageiros, permitindo decisões estratégicas baseadas nesse dados.

Funcionalidades:
- Captura de imagens em tempo real por câmeras instaladas nas estações.
- Detecção e reconhecimento facial de pessoas préviamente detectadas.
- Armazenamento temporário e sincronização diária de dados em banco central (que servirá de base de dados para o Metrô).
- Análise dos dados capturados e geração de resultados.

Tecnologias utilizadas:
- Backend: .NET 8.0, C#, FaceAISharp (biblioteca para reconhecimento facial)
- Infraestrutura em Cloud: Amazon AWS, AWS EC2
- Mensageria: AWS SQS
- Banco de Dados: AWS RDS, MongoDB
- Frontend (exclusivo para a disciplina): JavaScript, React JS

Contexto de uso:
- ADICIONAR CONTEXTO DE USO

A idealização do projeto (somente o sistema distribuído em larga escala, e a geração de dados para análise futura) não necessita de uma inteface, então inicialmente não prevemos o desenvolvimento de uma interface.

## Publico Alvo

O projeto é direcionado principalmente para organizações de transporte público urbano (nesse caso, especificamente o Metrô de São Paulo). Foi feita uma análise de expansão do projeto, e ele também pode alcançar como público alvo grandes centros movimentados (como shoppings, ou centros automotivos), pois criaria uma base de dados de fluxo baseado nas câmeras espalhadas pelo ambiente, e facilitaria a otimização da alocação de recursos operacionais, baseado na análise desses dados, similar ao Metrô.

Características do público-alvo:
- ADICIONAR CARACTERÍSTICAS

## Análise de concorrência

1. Identifique os principais concorrentes ou softwares mais utilizados pelo seu público-alvo.
2. Colete informações sobre os concorrentes selecionados.
3. Analise as características e funcionalidades dos concorrentes.
4. Avalie a experiência do usuário (UX).
5. Examine os preços e modelos de negócio.
6. Pesquisa de satisfação do cliente e opiniões.
7. Identifique padrões e tendências no mercado.
8. Elabore relatórios e sumarize os resultados.
9. Extraia pontos positivos e faça recomendações.

### Personas

- Descreva as personas que irão interagir com a aplicação ou produto. Deixe claro suas principais caracteristicas e contextos sociais, econômicos e culturais.
- Quais informações sobre o usuário o serviço ou poduto deve guardar?

  - Persona primaira ...
  - Persona secundária ...
  - Outras personas ...

### Mapa de empatia

![Mapa de empatia](empatia.png)

- Determine o mapa de empatia[^1] de pelo menos uma persona primária e uma sercundária.
  - O que o usuário vê: aqui estamos falando do ambiente visual em que o usuário se encontra. Ou seja, o que ele efetivamente enxerga, as pessoas e objetos que estão ao seu redor. Isso ajuda a entender o contexto em que o usuário está inserido e as influências visuais que está recebendo.
  - O que o usuário ouve: neste quadrante, buscamos entender o que o usuário está ouvindo, os sons que o cercam e como eles influenciam suas ações.
  - O que o usuário diz e faz: aqui consideramos ações e comportamentos que o usuário apresenta durante sua interação com serviço ou poduto.
  - O que o usuário pensa e sente: neste quadrante, buscamos entender os pensamentos, sentimentos, emoções e percepções que o usuário tem em relação ao serviço ou poduto. Quais expectativas o usuário cria sobre o serviço ou poduto?
  Que tipo de serviço ou poduto mais agrada essa persona?
  - Dores: quando falamos sobre dores do usuário, estamos fazendo referência a quaisquer obstáculos, necessidades ou frustrações que o usuário possa experimentar ao tentar realizar uma tarefa ou alcançar um objetivo. Isso inclui, por exemplo, problemas de usabilidade, dificuldades de acesso ou outros desafios que podem afetar a experiência do usuário.
  - Ganhos: nesse caso estamos falando de quaisquer benefícios ou recompensas que o usuário possa experimentar ao utilizar o serviço ou poduto. Isso pode incluir economia de tempo ou facilidade de uso, por exemplo. Que desejos do usuário o serviço ou poduto satisfaz?

## Contexto de uso

- Descreva o ambiente em que o serviço ou poduto deve ser utilizado.
- Qual/quais o(s) contexto(s) sociais, econômicos e culturais existentes neste ambiente?
- Quais informações sobre o ambiente, o serviço ou poduto deve guardar antes de iniciar a interação?
- O que normalmente deve estar acontecendo com o ambiente quando o usuário interagir com o serviço ou poduto?

## Jornada do usuário

- Criar uma narrativa para o o seu serviço ou poduto com o usuário.
- Determine o que o usuário realiza desde a primeira até o última interação com o serviço ou poduto.
  - Descreva o que acontece ou pode acontecer passo a passo
  - Como a tarefa começa? Como a tarefa se desenvolve? Como a tarefa termina?


<!--
## Análise de concorrência

- Pesquise serviços ou podutos existentes atualmente que possam realizar o objetivo deste projeto.
- Selecione pelo menos 3 serviços ou podutos diferentes.
- Em relação aos concorrentes, respondam as seguintes perguntas?
  - Existe plataforma similar que atende o mesmo mercado e funcionalidades? Se sim: Quais os pontos positivos? Quais os pontos negativos?
  - Existe plataforma diferente quanto ao serviço, mas que atenda esse mercado? Se sim: Quais os pontos positivos? Quais os pontos negativos?
 -->
 
## Coleta de dados

## Modelo de tarefas

## Design

- Pense nas características de Affordances do seu serviço ou poduto. 
    - Que tipo de acessibilidades devem ser consideradas dentro do seu projeto?
- Discuta o papel das expectativas do usuário no projeto deste serviço ou poduto. Qual a importância e pontos a serem considerados se você quiser vender esse serviço ou poduto?

### Prototipação em baixo nível (papel)
#### Avaliação heurística

### Prtotipação em médio nível (Figma)
#### Avaliação heurística

### Prtotipação em alto nível (React)
#### Avaliação heurística

[^1]: Fonte: Adaptado de <https://hazeshift.com.br/mapa-de-empatia/>

<!-- TODOs:
- Add exemplos
 -->
