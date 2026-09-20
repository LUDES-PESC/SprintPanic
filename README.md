# Sprint Panic! 🚀

**Sprint Panic!** é um jogo educacional sobre Scrum, fluxo de trabalho e tomada de decisão em projetos de software.

O jogador acompanha um time responsável por desenvolver um aplicativo interplanetário de entrega de pizzas. Ao longo de quatro Sprints, precisa definir objetivos, selecionar trabalho, lidar com imprevistos, controlar trabalho em andamento, participar de Daily Scrums, Sprint Reviews e Retrospectives e adaptar o plano sem perder de vista o Product Goal.

O jogo foi pensado para uso em aulas, treinamentos, workshops e estudo individual.

---

## Objetivo pedagógico

A proposta não é ensinar Scrum como uma sequência burocrática de cerimônias, mas mostrar como seus elementos se relacionam durante o desenvolvimento de um produto sob incerteza.

O jogo trabalha conceitos como:

- Product Goal;
- Product Backlog;
- Sprint Goal;
- Sprint Backlog;
- Incremento;
- Definition of Done;
- Sprint Planning;
- Daily Scrum;
- Sprint Review;
- Sprint Retrospective;
- adaptação do plano durante a Sprint;
- trabalho técnico emergente;
- impedimentos;
- dívida técnica;
- qualidade;
- feedback de stakeholders;
- WIP (*Work in Progress*);
- swarming;
- velocity;
- Burndown;
- Burnup;
- Cumulative Flow Diagram.

O jogo procura distinguir explicitamente os elementos definidos pelo **Scrum Guide** de práticas complementares frequentemente utilizadas por equipes Scrum.

Por exemplo, **Velocity, Burndown, Burnup, CFD e limites de WIP não são artefatos ou eventos obrigatórios do Scrum**. Eles aparecem como práticas de apoio à previsão, transparência e gestão do fluxo.

---

## Cenário

O produto é um aplicativo de entrega de pizzas para Marte.

### Product Goal

> Permitir que uma pessoa em Marte escolha, pague e acompanhe uma pizza com confiança.

O Product Backlog inclui funcionalidades como escolha da pizza, carrinho, endereço marciano, pagamento orbital, recibo, rastreamento, previsão de chegada, tratamento de falhas e acessibilidade.

---

## Como jogar

A partida possui **quatro Sprints**.

Cada Sprint representa cinco dias simulados de trabalho.

Fluxo básico:

1. escolher um **Sprint Goal**;
2. selecionar itens para o **Sprint Backlog**;
3. iniciar a Sprint;
4. acompanhar o trabalho do time;
5. responder a eventos e trabalho emergente;
6. participar do **Daily Scrum**;
7. realizar a **Sprint Review**;
8. realizar a **Sprint Retrospective**;
9. adaptar o Product Backlog e iniciar a Sprint seguinte.

O botão principal conduz o jogador pelas diferentes fases da simulação.

Sempre que o jogo exige uma decisão, a interface muda automaticamente para a área **Jogo**, onde aparecem a situação e as alternativas.

---

## Sprint Backlog e fluxo

Durante uma Sprint, o trabalho aparece em três estados:

```text
A FAZER → EM ANDAMENTO → DONE
```

O time possui três Developers.

O jogador pode iniciar ou pausar itens, reduzir WIP e concentrar Developers em um mesmo item.

### WIP

A simulação sugere aproximadamente **dois itens simultaneamente em andamento**.

Esse limite é uma **regra pedagógica da simulação**, não uma regra do Scrum Guide.

WIP excessivo reduz a eficiência simulada por representar troca de contexto, coordenação adicional e dificuldade para levar trabalho até Done.

### Swarming

Mais de um Developer pode trabalhar sobre o mesmo item.

A simulação utiliza retornos decrescentes:

```text
1 Developer  = 1,00×
2 Developers = 1,65×
3 Developers = 2,05×
```

---

## Velocity

O time é calibrado para uma **velocity típica entre 9 e 13 pontos por Sprint**, aproximadamente centrada em 11 pontos.

A primeira Sprint é deliberadamente mais simples, para que o jogador compreenda o fluxo e tenha alta probabilidade de atingir o primeiro Sprint Goal.

Nas Sprints seguintes, a previsão utiliza o histórico observado.

No jogo, velocity é apresentada como:

> evidência para previsão do próprio time, não como meta, medida individual de produtividade ou instrumento de comparação entre equipes.

Trabalho técnico emergente consome capacidade, mas não aumenta artificialmente a velocity de produto.

---

## Trabalho emergente

Problemas descobertos durante a Sprint não aumentam silenciosamente o tamanho de um PBI.

Quando surge trabalho necessário, ele pode aparecer explicitamente no Sprint Backlog.

Exemplo:

```text
💳 Pagamento orbital
└── ⚙️ Atualizar autenticação da API

🛰️ Rastrear entrega
└── 🐛 Corrigir erro de atualização de status
```

Esses itens podem representar trabalho técnico, defeitos, integração, atualizações de dependências, segurança ou infraestrutura.

Um PBI não pode chegar a Done enquanto possuir trabalho bloqueador ainda incompleto.

---

## Eventos

A partir da segunda Sprint, podem surgir eventos inesperados.

### Pessoas

- doença de uma pessoa do time;
- gripe afetando mais de um Developer;
- afastamento parcial;
- Product Owner temporariamente indisponível.

### Infraestrutura

- falta de energia;
- Internet fora do ar;
- VPN indisponível;
- notebook quebrado;
- certificado expirado;
- limite do serviço de CI;
- ambiente de testes instável.

### Dependências e bibliotecas

- Release Candidate (RC);
- patch com correções de bugs;
- atualização de segurança;
- nova versão major incompatível;
- mudanças de API e dependências.

### Engenharia

- testes flaky;
- conflito de merge;
- regressões;
- dependências ocultas;
- automação de testes;
- reutilização;
- cache de build.

Nem todo evento é negativo: alguns representam oportunidades de melhoria.

---

## Qualidade e dívida técnica

A simulação acompanha:

- valor entregue;
- qualidade;
- confiança dos stakeholders;
- dívida técnica.

Dívida técnica pode surgir quando o jogador, por exemplo:

- adia uma correção importante;
- aceita um risco de segurança;
- utiliza um workaround;
- tenta entregar antes da Definition of Done;
- troca qualidade por velocidade de curto prazo.

---

## Sprint Review

A Sprint Review não é tratada apenas como demonstração.

O jogador precisa interpretar feedback e decidir se ele deve:

- alterar a ordem do Product Backlog;
- registrar nova necessidade;
- manter a ordem atual até obter mais evidências;
- ajustar prioridades;
- reconsiderar riscos e condições de lançamento.

---

## Sprint Retrospective

Na Retrospective, o jogador escolhe melhorias relacionadas ao que ocorreu na Sprint, como:

- reduzir WIP;
- automatizar testes;
- melhorar refinamento;
- explicitar dependências;
- reduzir trabalho repetitivo;
- melhorar integração.

---

## Métricas e gráficos

O jogo apresenta:

- **Burndown** — trabalho restante durante a Sprint;
- **Burnup** — valor entregue versus escopo;
- **Cumulative Flow Diagram** — trabalho a fazer, em andamento e Done;
- **Velocity** — pontos de PBIs de produto concluídos por Sprint.

Essas visualizações apoiam a compreensão do fluxo e da previsão, mas não são apresentadas como componentes obrigatórios do Scrum.

---

## Internacionalização

O jogo está disponível em cinco idiomas:

- Português;
- English;
- Español;
- Français;
- Italiano.

O idioma é escolhido no **Setup**.

A tradução cobre interface, Sprint Goals, eventos, perguntas, alternativas, Daily Scrum, Sprint Review, Retrospective, feedback e debrief final.

---

## Interface

A interface foi pensada com prioridade para dispositivos móveis.

O topo possui uma barra fixa com:

- menu hambúrguer;
- título;
- Setup.

O menu permite acessar:

- Jogo;
- Product Backlog;
- Sprint Backlog;
- Burndown;
- Burnup;
- Fluxo;
- Velocity;
- Scrum;
- Debrief.

---

## Execução

Não há instalação, servidor ou dependências externas.

Basta abrir o arquivo HTML em um navegador moderno.

```text
sprint_panic.html
```

O jogo também pode ser publicado diretamente com **GitHub Pages**.

---

## Arquitetura

O projeto é deliberadamente uma **single-file application**.

Toda a aplicação está contida em um único HTML:

```text
HTML
CSS
JavaScript
dados
traduções
regras da simulação
gráficos
interface
```

Não são necessários:

- frameworks JavaScript;
- bibliotecas externas;
- backend;
- banco de dados;
- CDN;
- chamadas de rede.

Depois de carregado, o jogo pode funcionar totalmente offline.

---

## Estrutura sugerida do repositório

```text
/
├── README.md
├── sprint_panic.html
├── LICENSE
└── docs/
    └── screenshots/
```

O jogo em si continua sendo um único arquivo HTML.

---

## Uso em aula

Uma partida completa pode ser usada como:

- introdução ao Scrum;
- exercício após aula teórica;
- atividade em grupos;
- demonstração de fluxo;
- discussão sobre Product Backlog × Sprint Backlog;
- estudo de decisões sob incerteza;
- introdução a métricas ágeis.

Perguntas úteis para discussão:

1. Por que determinados Sprint Goals foram ou não alcançados?
2. Quando o time deveria reduzir WIP?
3. Quando trabalho técnico deve aparecer no Sprint Backlog?
4. Quando feedback deve alterar o Product Backlog?
5. Por que velocity não deve ser tratada como meta?
6. Quais decisões produziram dívida técnica?
7. Quais eventos deveriam ou não alterar o Sprint Goal?

---

## Referência conceitual

A principal referência é:

> Schwaber, K.; Sutherland, J. **The Scrum Guide — The Definitive Guide to Scrum: The Rules of the Game.** 2020.

<https://scrumguides.org/>

O jogo também incorpora práticas de fluxo e métricas frequentemente usadas em ambientes ágeis, procurando distingui-las dos elementos formais do Scrum Guide.

---

## Contribuindo

Contribuições são bem-vindas, especialmente:

- novos eventos;
- revisão das traduções;
- melhorias de acessibilidade;
- novos cenários;
- balanceamento;
- testes em dispositivos móveis;
- melhorias de interface;
- material didático;
- estudos sobre uso do jogo em aula.

Ao propor uma regra, é útil indicar se ela representa:

1. uma regra formal do Scrum;
2. uma prática comum;
3. uma simplificação pedagógica;
4. uma regra específica da simulação.

Essa distinção evita que decisões de game design sejam confundidas com prescrições do Scrum Guide.

---

## Créditos

**Sprint Panic!** foi concebido como um jogo educacional sobre Scrum, fluxo de trabalho e tomada de decisão em projetos de software.

Projeto desenvolvido no contexto de atividades de ensino e pesquisa em Engenharia de Software, Jogos e Simulações.

---

## Licença

Defina aqui a licença desejada para o projeto.

Opções comuns para software educacional aberto incluem MIT, BSD-3-Clause, Apache-2.0 e GPL-3.0.

Se o projeto estiver vinculado institucionalmente a uma universidade ou projeto de pesquisa, recomenda-se verificar também as regras institucionais aplicáveis antes de definir a licença definitiva.
