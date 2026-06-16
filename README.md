# \# 🏆 DESAFIO FINAL — Git \& GitHub Desktop

# \### Disciplina: Desenvolvimento de Sistemas | SENAI

# \### Nível: Individual | Ferramenta: GitHub Desktop

# ---

# 

# \## 🎯 O que muda neste desafio?

# 

# Nas atividades anteriores você \*\*corrigiu\*\* um código pronto.

# Agora você vai \*\*construir\*\* um projeto do zero — adicionando

# funcionalidades aos poucos e registrando cada etapa com Git.

# 

# É assim que funciona no mercado: o histórico de commits conta

# a história de como o projeto cresceu.

# 

# ---

# 

# \## 📋 Visão Geral do Desafio

# 

# Você vai construir um \*\*Sistema de Cadastro Escolar\*\* em 3 etapas,

# usando o GitHub Desktop para gerenciar tudo:

# 

# | Etapa | O que fazer | Ferramenta Git |

# |-------|-------------|----------------|

# | 1 | Criar o repo e fazer o commit inicial | GitHub Desktop |

# | 2 | Adicionar 8 funções, 1 commit por função | GitHub Desktop |

# | 3 | Criar uma branch, adicionar melhorias e fazer merge | GitHub Desktop |

# 

# ---

# 

# \## 🚀 ETAPA 1 — Criando o Repositório

# 

# \### Passo a passo no GitHub Desktop:

# 

# \*\*1.1 — Crie o repositório local\*\*

# \- Abra o \*\*GitHub Desktop\*\*

# \- Clique em `File` → `New Repository`

# \- Nome: `sistema-escola-final`

# \- Marque a opção \*\*Initialize this repository with a README\*\*

# \- Clique em `Create Repository`

# 

# \*\*1.2 — Adicione o arquivo do projeto\*\*

# \- Copie o arquivo `sistema\_escola\_v3.py` para a pasta do repositório

# \- No GitHub Desktop, você vai ver o arquivo aparecer na aba `Changes`

# 

# \*\*1.3 — Faça o commit inicial\*\*

# \- No campo `Summary`, escreva:

# &nbsp; ```

# &nbsp; feat: adiciona estrutura inicial do sistema escola

# &nbsp; ```

# \- Clique em `Commit to main`

# 

# \*\*1.4 — Publique no GitHub\*\*

# \- Clique em `Publish repository`

# \- Deixe o repositório como \*\*Public\*\*

# \- Clique em `Publish Repository`

# 

# ✅ \*\*Checkpoint:\*\* Acesse seu GitHub no navegador e confirme que o repositório aparece com 1 commit.

# 

# ---

# 

# \## 🔨 ETAPA 2 — Construindo as Funções (1 commit por função)

# 

# Para cada função abaixo, siga sempre este ritual:

# 

# ```

# 1\. Escreva a função no arquivo

# 2\. Rode o arquivo para testar (python sistema\_escola\_v3.py)

# 3\. No GitHub Desktop → veja as mudanças em "Changes"

# 4\. Escreva a mensagem de commit

# 5\. Clique em "Commit to main"

# 6\. Clique em "Push origin"

# ```

# 

# ---

# 

# \### Função 5 — `cadastrar\_aluno`

# Crie uma função que recebe `nome`, `turma` e `idade` e retorna um dicionário com esses dados.

# 

# ```python

# def cadastrar\_aluno(nome, turma, idade):

# &nbsp;   aluno = {

# &nbsp;       "nome": nome,

# &nbsp;       "turma": turma,

# &nbsp;       "idade": idade

# &nbsp;   }

# &nbsp;   return aluno

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao cadastrar\_aluno

# ```

# 

# ---

# 

# \### Função 6 — `exibir\_aluno`

# Crie uma função que recebe o dicionário do aluno e imprime os dados formatados.

# 

# ```python

# def exibir\_aluno(aluno):

# &nbsp;   print("==== DADOS DO ALUNO ====")

# &nbsp;   print(f"Nome : {aluno\['nome']}")

# &nbsp;   print(f"Turma: {aluno\['turma']}")

# &nbsp;   print(f"Idade: {aluno\['idade']} anos")

# &nbsp;   print("========================")

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao exibir\_aluno

# ```

# 

# ---

# 

# \### Função 7 — `calcular\_media`

# Crie uma função que recebe uma lista de notas e retorna a média.

# 

# ```python

# def calcular\_media(notas):

# &nbsp;   return sum(notas) / len(notas)

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao calcular\_media

# ```

# 

# ---

# 

# \### Função 8 — `verificar\_aprovacao`

# Crie uma função que recebe a média e retorna `"Aprovado"` se >= 6, ou `"Reprovado"` se menor.

# 

# ```python

# def verificar\_aprovacao(media):

# &nbsp;   if media >= 6:

# &nbsp;       return "Aprovado"

# &nbsp;   else:

# &nbsp;       return "Reprovado"

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao verificar\_aprovacao

# ```

# 

# ---

# 

# \### Função 9 — `gerar\_email`

# Crie uma função que gera um e-mail no formato `nome.turma@senai.br`.

# 

# ```python

# def gerar\_email(nome, turma):

# &nbsp;   nome\_formatado = nome.lower().replace(" ", ".")

# &nbsp;   return f"{nome\_formatado}.{turma.lower()}@senai.br"

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao gerar\_email

# ```

# 

# ---

# 

# \### Função 10 — `relatorio\_aluno`

# Crie uma função que recebe o dicionário do aluno (já com nota) e exibe o relatório completo.

# 

# ```python

# def relatorio\_aluno(aluno):

# &nbsp;   print("\\n======= RELATÓRIO =======")

# &nbsp;   print(f"Nome  : {aluno\['nome']}")

# &nbsp;   print(f"Turma : {aluno\['turma']}")

# &nbsp;   nota = aluno.get("nota", None)

# &nbsp;   if nota is not None:

# &nbsp;       media = calcular\_media(nota) if isinstance(nota, list) else nota

# &nbsp;       print(f"Média : {media:.1f}")

# &nbsp;       print(f"Status: {verificar\_aprovacao(media)}")

# &nbsp;       print(f"E-mail: {gerar\_email(aluno\['nome'], aluno\['turma'])}")

# &nbsp;   else:

# &nbsp;       print("Nota  : Não lançada")

# &nbsp;   print("=========================")

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao relatorio\_aluno

# ```

# 

# ---

# 

# ✅ \*\*Checkpoint:\*\* No GitHub Desktop, clique em `History`. Você deve ver \*\*7 commits\*\* no total (1 inicial + 6 funções). Mostre para o professor antes de continuar.

# 

# ---

# 

# \## 🌿 ETAPA 3 — Criando uma Branch de Melhorias

# 

# Agora você vai trabalhar como um dev profissional:

# novas funcionalidades entram em uma \*\*branch separada\*\*,

# não direto no `main`.

# 

# \### Passo 3.1 — Criar a branch

# 

# \- No GitHub Desktop, clique no menu `Current Branch` (no topo)

# \- Clique em `New Branch`

# \- Nome da branch: `melhoria/frequencia`

# \- Clique em `Create Branch`

# 

# > Você agora está na branch `melhoria/frequencia`. O `main` continua intacto.

# 

# ---

# 

# \### Função 11 — `calcular\_frequencia`

# Adicione na branch `melhoria/frequencia`:

# 

# ```python

# def calcular\_frequencia(aulas\_dadas, faltas):

# &nbsp;   presencas = aulas\_dadas - faltas

# &nbsp;   percentual = (presencas / aulas\_dadas) \* 100

# &nbsp;   return round(percentual, 2)

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao calcular\_frequencia na branch melhoria

# ```

# 

# ---

# 

# \### Função 12 — `situacao\_final`

# Ainda na branch `melhoria/frequencia`:

# 

# ```python

# def situacao\_final(media, frequencia):

# &nbsp;   if media >= 6 and frequencia >= 75:

# &nbsp;       return "✅ Aprovado"

# &nbsp;   elif frequencia < 75:

# &nbsp;       return "❌ Reprovado por falta"

# &nbsp;   else:

# &nbsp;       return "❌ Reprovado por nota"

# ```

# 

# \*\*Mensagem de commit:\*\*

# ```

# feat: adiciona funcao situacao\_final na branch melhoria

# ```

# 

# ---

# 

# \### Passo 3.2 — Fazer o Push da branch

# 

# \- Clique em `Publish Branch` no GitHub Desktop

# \- Acesse seu GitHub no navegador e confirme que a branch `melhoria/frequencia` aparece

# 

# ---

# 

# \### Passo 3.3 — Merge da branch no main

# 

# \- No GitHub Desktop, volte para o `main`:

# &nbsp; clique em `Current Branch` → selecione `main`

# \- Clique em `Branch` (menu superior) → `Merge into Current Branch`

# \- Selecione `melhoria/frequencia`

# \- Clique em `Create a merge commit`

# \- Clique em `Push origin`

# 

# ✅ \*\*Checkpoint final:\*\* Acesse o repositório no GitHub. Clique em `commits` e confirme que você tem \*\*pelo menos 10 commits\*\* e que a branch `melhoria/frequencia` aparece no histórico.

# 

# ---

# 

# \## 📊 Critérios de Avaliação

# 

# | Critério | Pontos |

# |----------|--------|

# | Repositório público criado e publicado | 10 pts |

# | Commit inicial com o arquivo base | 10 pts |

# | 6 funções adicionadas com 1 commit cada | 30 pts |

# | Mensagens de commit no padrão `feat:` | 15 pts |

# | Branch `melhoria/frequencia` criada e publicada | 15 pts |

# | Funções 11 e 12 na branch com commits corretos | 10 pts |

# | Merge da branch no main registrado | 10 pts |

# | \*\*TOTAL\*\* | \*\*100 pts\*\* |

# 

# ---

# 

# \## ⚠️ Regras

# 

# \- Cada função = 1 commit. Não adicione duas funções no mesmo commit.

# \- Funções 11 e 12 \*\*obrigatoriamente\*\* na branch `melhoria/frequencia`, nunca no `main` diretamente.

# \- O repositório deve estar \*\*público\*\* para o professor conseguir acessar.

# 

# ---

# 

# \## 💡 Como verificar se está tudo certo

# 

# No GitHub Desktop, clique em \*\*History\*\* e você deve ver algo assim:

# 

# ```

# Merge branch 'melhoria/frequencia'

# feat: adiciona funcao situacao\_final na branch melhoria

# feat: adiciona funcao calcular\_frequencia na branch melhoria

# feat: adiciona funcao relatorio\_aluno

# feat: adiciona funcao gerar\_email

# feat: adiciona funcao verificar\_aprovacao

# feat: adiciona funcao calcular\_media

# feat: adiciona funcao exibir\_aluno

# feat: adiciona funcao cadastrar\_aluno

# feat: adiciona estrutura inicial do sistema escola

# ```

# 

# Se o seu histórico se parece com isso — parabéns, você concluiu o desafio! 🎉

# 

# ---

# 

# \## 📤 Entrega

# 

# Link do repositório público no GitHub.

# Prazo: \_\_\_/\_\_\_/\_\_\_\_\_\_

# 

# ---

# 

# \*Dúvidas com o GitHub Desktop? Chame o professor — mas tente resolver sozinho primeiro!\* 💪

