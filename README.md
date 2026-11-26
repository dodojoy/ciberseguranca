# Seminário de Cibersegurança: P14, Prompt Injection em aplicações com LLM

**Disciplina:** Auditoria e Segurança da Informação, 8º período de Sistemas de Informação (UNIRIOS, 2026.2)
**Professor:** Ronierison Maciel
**Modalidade:** B (seminário técnico)

## Integrantes

- Joyce Maria Barbosa Teodoro
- Lucas Fernando de Souza Pereira

## Sobre o seminário

Prompt injection é um ataque em que instruções maliciosas, disfarçadas de conteúdo comum, levam um modelo de linguagem (LLM) a ignorar as regras da aplicação e seguir as ordens do atacante. É o primeiro risco do OWASP Top 10 para aplicações com LLM (LLM01). O problema vem da forma como esses sistemas funcionam: as instruções do desenvolvedor e os dados que o modelo lê chegam pelo mesmo canal, em linguagem natural.

O cenário real analisado é brasileiro. Em maio de 2026, na 3ª Vara do Trabalho de Parauapebas (PA), duas advogadas esconderam em uma petição um comando em letras brancas sobre fundo branco, mandando a IA "contestar de forma superficial" e não impugnar os documentos. O Galileu, ferramenta de IA da Justiça do Trabalho, detectou o trecho oculto e emitiu um alerta. O juiz aplicou multa de cerca de R$ 84,2 mil.

A partir do caso, discutimos as defesas de prevenção, detecção e mitigação, escolhemos a ferramenta mais adequada para o contexto de um tribunal e comparamos com cenários mais difíceis, como o EchoLeak, em que a mesma técnica fez o Microsoft 365 Copilot vazar dados.

**Pergunta central:** por que prompt injection ainda não tem solução definitiva, e como reduzir o dano quando ela acontece?

**Nossa resposta, em resumo:** a causa é estrutural, porque instrução e dado chegam ao modelo pelo mesmo canal e qualquer filtro é probabilístico. Por isso, a estratégia mais adequada é assumir que a injeção vai acontecer e projetar o sistema para limitar o dano: dar à IA só o poder necessário para a tarefa, manter a decisão final com pessoas e garantir que toda informação gerada possa ser conferida na fonte.

Nenhum ataque foi executado na preparação deste trabalho. Todo o conteúdo vem de pesquisa em fontes públicas.

## Arquivos entregues

| Arquivo              | Conteúdo                                      |
| -------------------- | --------------------------------------------- |
| `README.md`          | Este arquivo                                  |
| `apresentacao.pdf`   | Slides do seminário                           |
| `resumo-tecnico.pdf` | Resumo técnico                                |
| `referencias.md`     | Fontes consultadas, com link e data de acesso |

## Declaração de uso de Inteligência Artificial

**Ferramenta:** Claude (Anthropic).

**Para que usamos:**

- **Slides:** a IA montou a apresentação (estrutura, diagrama e layout) a partir do tema e do caso que escolhemos.
- **Busca de fontes:** a escolha do caso de Parauapebas foi nossa. A IA ajudou a encontrar fontes que tratavam dele (artigos, reportagens e documentação técnica) e a organizar as referências no padrão ABNT.
- **Texto do resumo técnico:** a IA ajudou a redigir e revisar as seções a partir das fontes que indicamos. Pedimos várias reescritas e definimos o recorte de cada parte, como a escolha da ferramenta de detecção para o caso.
- **README e referências:** a IA redigiu este README e o arquivo `referencias.md` a partir do conteúdo final do trabalho. Revisamos os dois antes da entrega.

**Como conferimos o resultado:**

- Abrimos cada referência na fonte original. Algumas fontes foram indicadas por nós, como o artigo de Alcântara no Migalhas, a reportagem do g1 e a do JOTA.
- Conferimos na fonte os números e fatos do caso: o texto do comando oculto, o valor da multa, a forma de detecção e a posição das advogadas.
- Revisamos todo o conteúdo entregue, e os dois integrantes conseguem explicá-lo na defesa.
