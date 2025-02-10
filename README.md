![Análise do Mercado de Ações](imagens/mercado-financeiro.gif)

O projeto **Análise do Mercado de Ações com Relatório por E-mail** foi desenvolvido para fornecer uma solução automatizada para a análise e monitoramento de importantes índices e ativos financeiros, como o Índice Bovespa (IBOV), o S&P 500 e a taxa de câmbio BRL/USD.

> O objetivo principal é coletar, visualizar e enviar mensalmente por e-mail relatórios com o desempenho desses ativos.

Isso permite que investidores e entusiastas do mercado financeiro tenham acesso a informações atualizadas e visualmente atraentes sobre o desempenho desses índices e ativos.

## Fontes de Dados
O projeto coleta os seguintes dados:

1. **IBOV (Índice Bovespa)**: Desempenho do mercado de ações brasileiro.
2. **S&P 500**: Um dos principais índices de ações dos Estados Unidos.
3. **BRL/USD**: Cotação do câmbio Real/US Dollar.

### Funcionalidades Detalhadas:
1. **Coleta de Dados Financeiros**
   
O projeto utiliza a biblioteca `yfinance` para coletar dados dos seguintes ativos:

- IBOV (Índice Bovespa): Representa o desempenho do mercado de ações brasileiro.

- S&P 500: Um dos principais índices de ações dos Estados Unidos.

- BRL/USD: Taxa de câmbio entre o Real brasileiro e o Dólar americano.

Os dados são coletados para um período de 6 meses por padrão, mas você pode ajustar o período no arquivo `config.py`.

2. **Geração de Gráficos**
   
Os gráficos são gerados usando as bibliotecas `matplotlib` e `mplcyberpunk` para um estilo visual moderno e atraente. Os gráficos incluem:

- Gráfico do Índice Bovespa (IBOV)

- Gráfico do S&P 500

- Gráfico da Taxa de Câmbio BRL/USD

Exemplo do gráfico:

![Gráfico IBOVESPA](imagens/ibovespa.png)

Os gráficos são salvos e anexados ao email.

3. **Cálculo de Retorno**
   
O projeto calcula o retorno percentual de cada ativo no período analisado. O retorno é exibido no corpo do email e pode ser usado para análises rápidas.

4. **Envio de Relatório por Email**
   
O relatório é enviado automaticamente usando a biblioteca `smtplib`. O email inclui:

Assunto: "Panorama do Mercado Financeiro"

Corpo do Email: Resumo dos retornos e instruções para visualizar os gráficos.

Anexos: Gráficos gerados em formato PNG.

Exemplo:

![Gráfico IBOVESPA](imagens/email-exemplo.jpeg)

## Conclusão

Ao finalizar a análise, você pode enviar automaticamente um email com os gráficos gerados anexados. O envio é realizado utilizando a biblioteca `smtplib`, e você pode personalizar facilmente o destinatário, o assunto, o corpo da mensagem e outros parâmetros diretamente no código. Essa funcionalidade garante que os relatórios sejam entregues de forma rápida e eficiente, sem necessidade de intervenção manual.

## Tecnologias Utilizadas:
- **Python 3.x:** Linguagem de programação principal.
- **Yahoo Finance API (yfinance):** Para coleta de dados financeiros.
- **Pandas:** Para manipulação e análise de dados.
- **Matplotlib e mplcyberpunk:** Para criação de gráficos estilizados.
- **Smtplib:** Para envio de e-mails com relatórios anexados.

Você pode instalá-las com o seguinte comando:
```
pip install yfinance pandas matplotlib mplcyberpunk smtplib
```

## Como Executar o Projeto
1. Clone o repositório:
Primeiro, clone o repositório para o seu ambiente local:
~~~
git clone https://github.com/seu-usuario/projeto-analise-de-dados-financeiro.git
cd projeto-analise-de-dados-financeiro
~~~

2.  Executar o Jupyter Notebook:

Inicie o Jupyter Notebook e abra o arquivo para explorar a análise e visualizações dos dados.
```bash

jupyter notebook projeto-email.ipynb

```
Para agendar a execução mensal do script, utilize o Cron (em Linux/macOS) ou o Agendador de Tarefas (em Windows).

## 📧 Configuração de Email (Gmail, Outlook, Apple Mail)

Servidores SMTP Comuns
Aqui estão as configurações SMTP para alguns provedores de email populares:

Provedor| Servidor SMTP| Porta|
Gmail| smtp.gmail.com| 587|
Outlook| smtp.office365.com| 587|
Yahoo| smtp.mail.yahoo.com| 465|

> [!IMPORTANT]
> Se você usa autenticação em dois fatores, gere uma **senha de aplicativo** no seu provedor de email e use-a no campo `EMAIL_PASSWORD`.

## Agendamento Automático
Para garantir que o relatório seja enviado mensalmente, configure o agendamento automático conforme descrito acima. Isso permite que você receba os relatórios sem precisar executar o script manualmente.

## 🤝 Contribuições

Sinta-se à vontade para fazer fork deste repositório, enviar issues ou fazer pull requests caso deseje melhorar ou expandir o projeto!
