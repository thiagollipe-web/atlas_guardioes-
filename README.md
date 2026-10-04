# Atlas — Guardiões da Humanidade

**Atlas** é um jogo educativo em HTML5/Canvas para estudar Ciências Humanas por meio de exploração, leitura de conceitos, interpretação de situações e associação de ideias.

O jogador atravessa regiões inspiradas em ruínas, paisagens, cidades e jardins de pensamento. Cada região representa uma disciplina e cada trilha acompanha uma etapa escolar.

A edição atual foi construída para funcionar em um único arquivo HTML, sem instalação de bibliotecas e sem conexão obrigatória com a internet.

## Conteúdo da edição

O jogo possui:

- **20 trilhas**;
- **200 capítulos**;
- **600 desafios principais**;
- **20 revisões finais**;
- explicações depois das respostas;
- dicas opcionais;
- caderno de campo;
- mapa da expedição;
- fragmentos colecionáveis;
- 6 roupas desbloqueáveis por experiência;
- 4 tons de pele para o personagem;
- personagem explorador ou exploradora;
- salvamento automático;
- exportação e importação do progresso;
- controles por teclado, toque e botões na tela;
- opção de acesso sem caminhar.

Cada capítulo possui três momentos:

1. **Observar** — identificar um conceito a partir de uma pista;
2. **Investigar** — analisar uma situação-problema;
3. **Conectar** — associar três conceitos às suas explicações.

Depois de dez capítulos, a trilha libera uma revisão final com cinco questões.

## Organização por etapa escolar

| Etapa | História | Geografia | Filosofia | Sociologia |
|---|:---:|:---:|:---:|:---:|
| 6º ano do Ensino Fundamental | ✓ | ✓ | — | — |
| 7º ano do Ensino Fundamental | ✓ | ✓ | — | — |
| 8º ano do Ensino Fundamental | ✓ | ✓ | — | — |
| 9º ano do Ensino Fundamental | ✓ | ✓ | — | — |
| 1ª série do Ensino Médio | ✓ | ✓ | ✓ | ✓ |
| 2ª série do Ensino Médio | ✓ | ✓ | ✓ | ✓ |
| 3ª série do Ensino Médio | ✓ | ✓ | ✓ | ✓ |

A divisão do Ensino Médio é uma proposta didática para organizar o jogo. Ela pode ser adaptada ao planejamento da escola, ao currículo estadual ou à sequência utilizada pelo professor.

## Direção visual 32-bit

A arte recebeu uma direção **32-bit inspirada nos RPGs clássicos**, com acabamento mais detalhado e maior profundidade visual. O termo descreve a linguagem artística; o navegador continua renderizando a cena como Canvas 2D em cores RGBA.

A atualização visual inclui:

- personagens com contorno, roupas, mochila, mãos, botas, cabelo, rosto e variações de tom de pele;
- árvores com tronco, galhos, folhas em camadas, reflexos e frutos;
- ruínas com colunas, rachaduras, blocos, trepadeiras e partes iluminadas;
- casas com telhas, janelas, portas, chaminé e vasos;
- observatórios com cúpula, janelas, telescópio e brilho central;
- tendas com tecido dividido em planos, cordas, estacas e fogueira;
- cristais de missão com brilho, aura, anéis e estados diferentes;
- fragmentos colecionáveis com halo e partículas;
- sombras projetadas e luz ambiente;
- névoa, linhas de luz, partículas flutuantes e vinheta cinematográfica;
- paisagens específicas para História, Geografia, Sociologia e Filosofia;
- desenho em resolução interna ampliada para telas de alta densidade, com limite adaptativo para evitar excesso de memória;
- cenário decorativo rasterizado uma vez, deixando a animação concentrada nos elementos interativos;
- marcos, fragmentos, NPCs e jogador em uma camada superior para não desaparecerem atrás das copas.

Todos os elementos visuais são desenhados pelo próprio Canvas. O jogo não depende de imagens externas, sprites baixados ou CDN.

## Como jogar

1. Abra o arquivo `atlas_guardioes_da_humanidade.html`.
2. Digite o nome do explorador.
3. Escolha o ano ou a série.
4. Escolha uma trilha.
5. Leia a mensagem inicial.
6. Caminhe até o cristal dourado ou use **Seguir objetivo**.
7. Interaja com o marco para abrir o desafio.
8. Leia a explicação depois de responder.
9. Recupere os três marcos de cada capítulo.
10. Complete os dez capítulos e enfrente a revisão final.

Não existe cronômetro. Errar não apaga o progresso: a questão pode ser refeita e a explicação permanece disponível.

## Controles

| Ação | Teclado | Celular/tablet |
|---|---|---|
| Caminhar | Setas ou WASD | Direcional na tela |
| Interagir | E, Enter ou Espaço | Botão A ou botão central |
| Mapa | M ou B | Botão do mapa ou B |
| Caderno | N | Botão do caderno |
| Bolsa | I | Botão da bolsa |
| Tela cheia | F | Botão de tela cheia |
| Opções | Esc | Botão de opções |
| Fechar painel | Esc | Botão × |

A opção **Acesso sem caminhar**, nas configurações, permite abrir a atividade atual por botão. Ela foi incluída para reduzir a barreira causada pela navegação no mapa.

## Salvamento

O progresso é salvo automaticamente no armazenamento local do navegador. O jogo guarda:

- nome e personagem;
- série selecionada;
- trilhas iniciadas;
- capítulos concluídos;
- erros e estrelas de cada capítulo;
- fragmentos encontrados;
- roupas e experiência;
- posição recente na trilha;
- conclusão da revisão final.

O botão **Exportar progresso** cria o arquivo `atlas-progresso.json`. O botão **Importar progresso** permite restaurar esse arquivo em outro navegador ou aparelho.

Antes de limpar os dados do navegador, trocar de aparelho ou publicar uma nova versão, exporte uma cópia do progresso.

## Execução offline

O jogo não precisa de servidor para funcionar.

### Abrir diretamente

No computador, abra o arquivo HTML com duplo clique.

No Android, abra o arquivo pelo gerenciador de arquivos e selecione um navegador compatível.

### Usar um servidor local opcional

O servidor local pode melhorar a compatibilidade de alguns navegadores:

```bash
python3 -m http.server 8000
```

Depois, abra:

```text
http://127.0.0.1:8000/atlas_guardioes_da_humanidade.html
```

Esse servidor é apenas uma alternativa local. O jogo não envia perguntas, respostas ou progresso para um servidor.

## Acessibilidade e adaptação pedagógica

A interface combina Canvas para o mundo e HTML semântico para textos, menus, perguntas e explicações. O projeto inclui:

- textos de estudo fora do Canvas, facilitando seleção e leitura;
- diálogos com foco de teclado;
- botões com rótulos acessíveis;
- navegação por Tab, Enter e Espaço;
- perguntas sem limite de tempo;
- dicas abertas sob demanda;
- explicação para respostas corretas e incorretas;
- controle de movimento reduzido por meio do acesso sem caminhar;
- opção de reduzir animações;
- layout para celular em retrato e paisagem;
- controles ampliados para toque.

Para uso em sala, o professor pode pedir que os alunos anotem a justificativa antes de escolher a alternativa. O jogo foi pensado para provocar interpretação e comparação, não apenas memorização.

## Abordagem de conteúdo

As trilhas trabalham temas como:

- fontes históricas, tempo, memória e patrimônio;
- povos africanos, indígenas e sociedades americanas;
- colonização, escravidão, resistências e abolição;
- revoluções, industrialização, guerras, ditaduras e democracia;
- paisagem, território, cartografia, clima, água e biomas;
- população, migração, urbanização, indústria e desigualdades;
- globalização, geopolítica, energia, ambiente e justiça climática;
- atitude filosófica, conhecimento, ética, política e estética;
- cultura, trabalho, socialização, desigualdades, cidadania e movimentos sociais.

Os capítulos usam linguagem introdutória e situações autorais. Eles podem servir como revisão, atividade de recuperação, estação de aprendizagem ou ponto de partida para uma aula. O jogo não substitui livros, aulas, fontes primárias ou a mediação docente.

## Referências curriculares

A organização geral foi inspirada na área de Ciências Humanas e Sociais Aplicadas e em temas de História e Geografia presentes na BNCC.

- [BNCC — Ministério da Educação](https://basenacionalcomum.mec.gov.br/images/BNCC_EI_EF_110518_versaofinal_site.pdf)
- [Currículo Paulista — Ensino Médio](https://efape.educacao.sp.gov.br/curriculopaulista/ensino-medio/)

Os links aparecem no guia interno do jogo e só são acessados se o usuário clicar neles. O conteúdo do jogo está incorporado no HTML e permanece disponível offline.

## Estrutura técnica

O projeto foi mantido em um único arquivo para facilitar distribuição, aula e publicação:

```text
atlas_guardioes_da_humanidade.html
├── estilos CSS
├── interface HTML
├── dados curriculares em JSON embutido
├── motor de exploração em Canvas 2D
├── renderização da arte 32-bit
├── sistema de trilhas e desafios
├── salvamento local
└── controles de teclado e toque
```

As principais fronteiras do código são:

- **dados** — trilhas, capítulos, conceitos e questões;
- **estado** — personagem, progresso, posição, itens e trilhas concluídas;
- **simulação** — movimento, rotas, interação e desbloqueios;
- **renderização** — mundo, personagens, estruturas, cristais e efeitos;
- **interface** — caderno, mapa, bolsa, opções e desafios;
- **persistência** — `localStorage`, exportação e importação JSON.

A chave de armazenamento usada pelo jogo é:

```text
atlas.humanidades.v1
```

## Arquivos desta entrega

- `atlas_guardioes_da_humanidade.html` — jogo completo, independente e offline;
- `README.md` — documentação do projeto, conteúdo e uso.

## Validação realizada

A edição foi conferida em duas camadas:

- o motor atualizado passa no verificador de sintaxe JavaScript;
- o HTML final não contém placeholders de montagem e continua autocontido;
- a contagem de conteúdo confirma 20 trilhas, 200 capítulos e 600 associações de conceitos;
- o ciclo funcional de base cobre carregamento offline, navegação por teclado, controles de toque, telas de 320 px e 390 px, paisagem, painéis, trilha completa, novas tentativas, desbloqueios, revisão final, salvamento, exportação, importação e rotas dos 20 mapas;
- a atualização visual foi feita dentro das funções de renderização do Canvas, preservando a estrutura de perguntas, progresso e persistência;
- a ordem de camadas e o custo de desenho foram revisados para evitar obstrução de objetivos e sobrecarga por gradientes em cada frame.

A repetição do smoke test visual nesta sessão ficou impedida pelo navegador local de teste, que encerrou com falha antes de abrir qualquer página. Isso é uma limitação do ambiente de validação; o arquivo entregue segue independente e pronto para abrir no navegador do usuário.

## Licença

A licença de distribuição não foi definida nesta edição. Antes de publicar o projeto em um repositório público ou incorporá-lo a um produto, escolha uma licença adequada e registre a autoria, as contribuições e as condições de uso.
