# Análise de Subdomínios e Hosts

## Sobre

Este é um script bash simples para realizar a análise de subdomínios e hosts em um site específico. O script faz uso do comando `wget` para baixar o conteúdo da página web e, em seguida, extrai os URLs para identificar os subdomínios e hosts associados.

## Como Usar

1. **Execução do Script:**
   ```bash
   ./parshing.sh
Entrada do Usuário:

O script solicitará ao usuário que insira o endereço (URL) do site que deseja analisar.
Download da Página Web:

Utiliza o comando wget para baixar o conteúdo da página web especificada pelo usuário e salva-o como index.html.
Extração de URLs:

Utiliza grep para extrair URLs da página HTML.
Usa cut para obter apenas os domínios.
Utiliza sort -u para ordenar e remover duplicatas.
A lista resultante é salva no arquivo lista.
Exibição de Domínios e Hosts Encontrados:

O script exibe a lista de domínios e hosts encontrados na página.
Busca de Endereços IP:

Um loop while read é usado para iterar sobre cada linha da lista de domínios e hosts (lista).
Para cada domínio, o script usa o comando host para obter os endereços IP correspondentes.
Utiliza grep para filtrar as linhas que contêm "has address", exibindo os endereços IP.
Remoção de Arquivos Temporários:

Remove os arquivos temporários criados durante o processo.
Requisitos
O script requer o comando wget para baixar a página web.
Certifique-se de ter as permissões adequadas para executar o script (chmod +x parshing.sh).
Exemplo de Saída
less
Copy code
PARSING
Digite o endereço para buscar os domínios-host
https://example.com
Domínios e hosts encontrados:
example.com
subdomain1.example.com
subdomain2.example.com
Endereços IP dos domínios e hosts:
example.com has address 93.184.216.34
subdomain1.example.com has address 192.168.1.1
subdomain2.example.com has address 192.168.1.2
