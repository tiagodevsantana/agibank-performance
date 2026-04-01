# Projeto de Teste de Performance com JMeter

## Visão Geral

Este projeto tem como objetivo validar a performance da aplicação BlazeDemo utilizando o Apache JMeter para simulação de carga e análise de comportamento sob estresse.
O fluxo contempla a execução do teste, geração de relatório HTML e publicação do resultado via GitHub Pages, permitindo visualização acessível e compartilhamento com avaliadores.

## Objetivo

- Avaliar o tempo de resposta da aplicação sob carga
- Identificar possíveis gargalos de performance
- Validar a estabilidade do sistema durante execução contínua
- Demonstrar boas práticas em testes de performance e exposição de resultados

## Cenário de Teste

- Simulação de múltiplos usuários simultâneos
- Execução contínua por período determinado (ex: 300 segundos)
- Requisições realizadas na aplicação BlazeDemo
- Coleta de métricas de performance em tempo real

## Tecnologias Utilizadas

- Apache JMeter
- Java
- Git
- GitHub
- GitHub Pages
- Claude Code
- Augment IA

## Estrutura do Projeto
├── index.html
├── content/
├── sbadmin2-1.0.7/
├── BlazeDemo.jmx
├── statistics.json
├── resultado.jtl
└── README.md

## Como Executar o Teste

### Pré-requisitos

- Java instalado
- Apache JMeter instalado

### Execução via Interface Gráfica

1. Abrir o Apache JMeter  
2. Carregar o arquivo BlazeDemo.jmx  
3. Executar o teste clicando em Start  

### Execução via Linha de Comando

> jmeter -n -t BlazeDemo.jmx -l resultado.jtl -e -o report

## Relatório de Performance

O relatório foi gerado automaticamente pelo JMeter e publicado via GitHub Pages.

Acesse o dashboard interativo:

https://tiagodevsantana.github.io/agibank-performance/

## Análise de Performance

### Principais Métricas

Throughput: ~260–280 req/s
Tempo médio: ~800ms – 1100ms
Percentil 90: < 2s
Taxa de erro: ~0.01%

### Interpretação

Durante a execução do teste, foi possível observar:

- O sistema apresentou comportamento estável/instável sob carga  
- O tempo de resposta variou conforme o aumento de usuários simultâneos  
- Não houve falhas críticas / Houve degradação em cenários específicos  

### Pontos de Atenção

- Possível aumento de latência em picos de carga  
- Necessidade de otimização em endpoints com maior tempo de resposta  
- Importância de monitoramento contínuo em produção  

### Conclusão

O sistema demonstrou capacidade de suportar a carga simulada dentro dos parâmetros definidos.

Recomendações:

- Avaliar escalabilidade da infraestrutura conforme crescimento de usuários  
- Otimizar endpoints críticos  
- Implementar monitoramento de performance contínuo  

## Publicação do Relatório

O projeto utiliza GitHub Pages para disponibilizar o relatório.

Passos realizados:

1. Execução do teste via JMeter  
2. Geração do relatório HTML  
3. Organização dos arquivos na raiz do projeto  
4. Versionamento com Git  
5. Publicação no GitHub  
6. Configuração do GitHub Pages (branch main / root)  

## Boas Práticas Aplicadas

- Execução de testes via linha de comando para automação  
- Separação entre script de teste e resultados  
- Uso de métricas relevantes (P90, P95, throughput)  
- Publicação de resultados para fácil acesso  
- Documentação estruturada e objetiva  

## Autor

Tiago Santana  
QA Engineer SR

LinkedIn: https://www.linkedin.com/in/tssqa/

## Considerações Finais

Este projeto demonstra a execução de testes de performance aliada à análise de métricas e comunicação dos resultados, permitindo suporte à tomada de decisão técnica e estratégica.
