# 🛡️ Análise de Tráfego de Rede: Vulnerabilidade no Protocolo HTTP

### 📋 Descrição do Projeto
Este projeto demonstra, de forma prática, a fragilidade de protocolos que não utilizam criptografia (cleartext). Através da ferramenta **Wireshark**, realizei a interceptação de pacotes em uma rede local para analisar a comunicação entre um cliente e um servidor web via HTTP.

### 🛠️ Ferramentas Utilizadas
* **Wireshark:** Captura e análise de pacotes.
* **Sistema Operacional:** Windows / Linux (WSL).
* **Protocolo Analisado:** HTTP (Porta 80).

### 🔍 Metodologia
1. Iniciei a captura de pacotes na interface de rede ativa.
2. Acessei o host `info.cern.ch` via navegador.
3. Filtrei o tráfego capturado utilizando o filtro `http`.
4. Utilizei a função `Follow TCP/HTTP Stream` para reconstruir a conversa entre as máquinas.

### 📊 Resultados
Como demonstrado na imagem abaixo, é possível ler toda a estrutura do site, informações do navegador e cabeçalhos de resposta do servidor em texto puro:

<img width="1276" height="1000" alt="Captura de tela 2026-03-05 221037" src="https://github.com/user-attachments/assets/02839e66-c912-49fe-9ce7-6c032d95fb5d" />

### ✅ Conclusão
O experimento comprova que qualquer dado trafegado via HTTP pode ser lido por um atacante posicionado na mesma rede (Man-in-the-Middle). Isso reforça a necessidade crítica da implementação do **HTTPS (TLS/SSL)** para garantir a confidencialidade e integridade da informação.# wireshark-http-analysis
