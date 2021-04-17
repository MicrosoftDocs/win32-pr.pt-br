---
title: Cenário 1 exemplo de tempo limite HTTP usando o rastreamento ETW e comandos netsh
description: Por meio do rastreamento ETW, o fluxo de dados por meio do componente API do servidor HTTP pode ser inspecionado para diagnosticar problemas.
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa50f438aca664651b24db822f2b9e3a30da4682
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571048"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>Cenário 1: exemplo de tempo limite HTTP usando o rastreamento ETW e comandos netsh

Por meio do rastreamento ETW, o fluxo de dados por meio do componente API do servidor HTTP pode ser inspecionado para diagnosticar problemas. Por exemplo, os usuários de um aplicativo Web podem ver mensagens de erro no navegador que uma página da Web não pode exibir. No servidor que hospeda o aplicativo Web, o profissional de ti também vê uma entrada de tempo limite de conexão dentro do log de erros HTTP, como mostra a Figura 1 abaixo. O log de erros HTTP pode ser encontrado no seguinte diretório:% WINDIR% \\ System32 \\ LogFiles \\ Httperr \\ .

![Captura de tela que mostra a janela de comando netsh H T T que exibe um log de erros H T T P para tempo limite.](images/httperrorlog.png)

Figura 1: log de erros HTTP para tempo limite

## <a name="generating-an-etw-trace-report"></a>Gerando um relatório de rastreamento ETW

Para gerar um relatório de rastreamento ETW para o componente de API do servidor HTTP, execute as etapas abaixo no prompt de comando. Neste exemplo, o rastreamento é executado no servidor, já que está hospedando o aplicativo Web.

As etapas a seguir geram um rastreamento chamado Httptrace. ETL e, em seguida, convertem o rastreamento em um arquivo CSV chamado httptrace.csv. Como mostrado abaixo, o provedor de ETW para a API do servidor HTTP é chamado Microsoft-Windows-HttpService. A opção de linha de comando 0xFFF indica que todos os eventos ETW para esse provedor devem ser capturados.

**Gerar um relatório de rastreamento do ETW**

1.  Iniciar rastreamento ETW para componente de API do servidor HTTP: l **ogman.exe iniciar Httptrace-p Microsoft-Windows-HttpService 0xFFFF-o Httptrace. etl – ETS**
2.  Reproduza o problema para que ele possa ser capturado no rastreamento. Neste exemplo, acesse o aplicativo Web de um computador cliente, resultando na mensagem "a **página não pode ser exibida**" mostrada no cliente.
3.  Agora que o problema foi reproduzido, pare o rastreamento: **logman.exe parar Httptrace – ETS**
4.  Converter o relatório em formato CSV: **tracerpt.exe Httptrace. etl-de CSV-o httptrace.csv**
5.  Exiba o relatório de rastreamento. Um trecho de um rastreamento CSV é mostrado abaixo na tabela 1.

## <a name="viewing-the-trace-and-diagnosing"></a>Exibindo o rastreamento e diagnosticando

O arquivo CSV resultante para rastreamentos pode ser exibido no Excel ou em qualquer ferramenta que dê suporte ao formato CSV. A tabela 1 abaixo mostra os trechos de um arquivo de rastreamento de exemplo (httptrace.csv). No relatório de rastreamento, a coluna "nível" mostra uma entrada com um valor de "3", que corresponde a um aviso no ETW. O componente de API do servidor HTTP segue os níveis de ETW definidos no seguinte artigo: ( https://msdn2.microsoft.com/library/aa382793.aspx) . Os níveis de ETW incluem:



| Nível | Significado      |
|-------|--------------|
| 1     | Crítico     |
| 2     | Erro        |
| 3     | Aviso      |
| 4     | Infomational |
| 5     | Detalhado      |



 

Com esse aviso, o tipo de evento (coluna de tipo) relata "ConnTimedOut". Nas colunas subsequentes para o evento ConnTimeOut, o temporizador específico que expirou é relatado como "timer \_ ConnectionIdle". Observe que a coluna com a entrada "timer \_ ConnectionIdle" não está incluída na tabela para fins de brevidade e evite o trecho de colunas não contíguas.



| Nome do evento                    | Tipo            | ID do evento | Versão | Canal | Nível |
|-------------------------------|-----------------|----------|---------|---------|-------|
| EventTrace                    | parâmetro          | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | AddUrl          | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgReqQueueProp | 30       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect     | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn     | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq         | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Analisar           | 2        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | LogFileWrite    | 51       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnCleanup     | 24       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnTimedOut    | 53       | 0       | 16      | 3     |



 

Tabela 1: trechos de um relatório de rastreamento de exemplo para um problema de temporizador

Neste exemplo, a expiração (evento ConnTimeOut) do temporizador de cabeçalho (temporizador \_ ConnectionIdle) é o motivo pelo qual os usuários finais veem a mensagem "a página não pode ser exibida" em seus clientes Web. Um motivo em potencial para o tempo limite pode ser que os clientes da Web estão enviando lentamente devido a conexões lentas. Para resolver esse problema, o valor de tempo limite pode ser ajustado por meio de comandos netsh.

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>Ajustando o tempo limite por meio do netsh e verificando a solução

Os comandos netsh para HTTP listados abaixo permitem que um profissional de ti exiba e defina valores de configuração no componente de API do servidor HTTP. As alterações por meio de comandos netsh HTTP afetam todos os aplicativos de servidor hospedados pelo componente de API do servidor HTTP para esse computador. Essas alterações persistem entre as reinicializações do componente e reinicializações do computador. Os comandos netsh HTTP estão disponíveis no Windows Vista e no Windows Server 2008 e substituem a ferramenta de HttpCfg.exe do Windows Server 2003 Resource Kit durante a execução no Windows Vista e no Windows Server 2008. Nesse cenário, ajustaremos um valor de tempo limite e, em seguida, verificaremos a solução. Existem temporizadores no componente de API do servidor HTTP para garantir a disponibilidade e proteger contra o excesso de consumo por um usuário mal configurado ou mal-intencionado. O ajuste de temporizadores de valores padrão deve ser avaliado cuidadosamente em relação a um ataque de DoS potencial.

Neste exemplo, os clientes Web estão atrás de uma conexão de rede lenta, resultando no \_ evento ETW ConnectionIdle do temporizador. Depois de considerar a causa dos tempos limite e do balanceamento com o impacto na carga do servidor, a decisão será feita para aumentar os valores de tempo limite para um valor de 240 segundos. Você pode exibir e, em seguida, configurar o temporizador com o procedimento a seguir.

**Configurar o temporizador de conexão ociosa (temporizador \_ ConnectionIdle) com netsh**

1.  No servidor, abra uma janela de comandos com privilégios elevados e execute as etapas abaixo para exibir e configurar o valor de tempo limite. Uma captura de tela do comando netsh HTTP é mostrada na Figura 2 abaixo.
2.  Mostrar os valores de tempo limite atuais: **netsh http show Timeout**
3.  Configure o valor de tempo limite de ConnectionIdle do temporizador \_ . Neste exemplo, o valor é alterado para 240 segundos: **netsh http add tempo_limite Timeout = idleConnectionTimeout valor = 240**

![janela de comando netsh http](images/netshhttpcommand.png)

Figura 2: janela de comando netsh HTTP

Depois de configurar o valor de tempo limite, execute novamente as etapas de diagnóstico ETW. Se a condição de erro for corrigida, o rastreamento ETW não deverá mais mostrar um tempo limite com um nível de ETW de "3" para o temporizador ocioso de conexão.

 

 




