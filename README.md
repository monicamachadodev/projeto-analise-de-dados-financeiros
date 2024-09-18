# 📊 Projeto de Análise de Dados Financeiros

Este projeto realiza a análise de dados financeiros de importantes índices e ativos, como o Índice Bovespa (IBOV), o S&P 500 e a taxa de câmbio BRL/USD. 

O objetivo principal é coletar, visualizar e enviar mensalmente por e-mail relatórios com o desempenho desses ativos.

## 🔍 Descrição do Projeto
O projeto utiliza a biblioteca **Yahoo Finance** para obter dados diários dos índices financeiros e cria gráficos para ilustrar o desempenho de cada ativo ao longo de um período de 6 meses.

Após a criação dos gráficos, eles são automaticamente enviados por email para o destinatário especificado. Esse envio ocorre com um relatório mensal anexado, tornando o processo automatizado e fácil de gerenciar.

## ⚙️ Funcionalidades
- **Coleta de dados financeiros** de índices e ativos como IBOV, S&P 500 e BRL/USD.
- **Criação de gráficos** detalhados do desempenho de cada ativo ao longo de um mês.
- **Envio automatizado de relatórios por email** com gráficos anexados para um destinatário pré-definido.

## 🛠️ Tecnologias Utilizadas
- **Python 3.x**
- **Yahoo Finance API (yfinance)**: Para obter dados financeiros.
- **Pandas**: Para manipulação de dados.
- **Matplotlib e mplcyberpunk**: Para visualização de dados e geração de gráficos estilizados.
- **Smtplib**: Para o envio de emails com relatórios anexados.

## 📊 Análise Financeira Realizada
O projeto coleta os seguintes dados:

1. **IBOV (Índice Bovespa)**: Desempenho do mercado de ações brasileiro.
2. **S&P 500**: Um dos principais índices de ações dos Estados Unidos.
3. **BRL/USD**: Cotação do câmbio Real/US Dollar.

Esses dados são coletados em um intervalo de 6 meses e processados para gerar gráficos que mostram as flutuações de preço ao longo do semestre.

## ✉️ Relatório por Email
Ao final do processo, o projeto envia automaticamente um email contendo os gráficos gerados como anexos. O relatório é enviado utilizando a biblioteca **smtplib**, e você pode configurar o destinatário e outros parâmetros diretamente no código.

Exemplo de email enviado:

- Assunto: Relatório Financeiro Mensal
- Corpo do email: "Segue em anexo o relatório financeiro mensal."
- Anexos: Gráficos de desempenho de IBOV, S&P 500 e BRL/USD.
![Gráfico IBOVESPA](imagens/email-exemplo.png)

## 📈 Exemplo de Gráficos
O projeto gera gráficos com o estilo **cyberpunk** para representar o desempenho dos índices e ativos de forma visualmente atraente.

Exemplos de gráficos gerados:

- Gráfico do Índice Bovespa (IBOV)
- Gráfico do S&P 500
- Gráfico da taxa de câmbio BRL/USD

![Gráfico IBOVESPA](imagens/ibovespa.png)


## 🚀 Como Executar o Projeto
1. Clone o repositório:

```bash
git clone https://github.com/seu-usuario/projeto-financeiro.git
cd projeto-financeiro
```

2. Execute o script no terminal no ambiente linux(deve estar instalado o jupyter notebook):

```bash

jupyter notebook projeto-email.ipynb

```
Para agendar a execução mensal do script, utilize o Cron (em Linux/macOS) ou o Agendador de Tarefas (em Windows).

## 📧 Configuração do Email
No código Python, você deve configurar as informações de email:

- Servidor SMTP
- Porta
- Usuário (seu email)
- Senha
- Destinatário do email

**Exemplo:**

```bash
servidor = "smtp.seuprovedor.com"
porta = 587
usuario = "seuemail@dominio.com"
senha = "suasenha"
destinatario = "destinatario@dominio.com"
```
Certifique-se de alterar essas configurações para garantir que o email seja enviado corretamente.

## 📅 Agendamento Automático
Este projeto pode ser configurado para rodar automaticamente uma vez por mês utilizando:

- Cron (Linux/macOS): Crie uma tarefa agendada que execute o script Python uma vez por mês.
- Task Scheduler (Windows): Configure o Agendador de Tarefas para rodar o script mensalmente.
