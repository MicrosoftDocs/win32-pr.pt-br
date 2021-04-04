---
title: Exemplo de analisador de cenário 2 usando o rastreamento ETW
description: Para gerar um relatório de rastreamento ETW para o componente de API do servidor HTTP, execute as etapas conforme mostrado na pasta \ 0034; Gerando um relatório de rastreamento ETW \ 0034; seção do exemplo de tempo limite HTTP de cenário 1 usando o rastreamento ETW e comandos netsh, mas reproduza o erro específico para esse cenário.
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c566973b660e4e665226fbf9b4a266b086b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007560"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>Cenário 2: exemplo do analisador usando o rastreamento ETW

Para gerar um relatório de rastreamento ETW para o componente de API do servidor HTTP, execute as etapas conforme mostrado na seção "gerando um relatório de rastreamento ETW" do [cenário 1: exemplo de tempo limite http usando o rastreamento ETW e comandos netsh](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md), mas reproduza o erro específico para esse cenário. Neste exemplo, acesse o aplicativo Web de um computador cliente, resultando na mensagem "400 solicitação inadequada" que está sendo mostrada no cliente. Essas etapas são executadas no servidor, já que ele está hospedando o aplicativo Web.

## <a name="viewing-the-trace-and-diagnosing"></a>Exibindo o rastreamento e diagnosticando

O arquivo CSV resultante para rastreamentos pode ser exibido no Excel ou em qualquer ferramenta que dê suporte ao formato CSV. A tabela 2 abaixo mostra trechos de um arquivo de rastreamento de exemplo (httptrace.csv). No relatório de rastreamento, a coluna "nível" mostra uma entrada com um valor de "2", que representa um erro. Conforme observado acima, o componente de API do servidor HTTP segue os níveis de ETW definidos no artigo [tipo complexo tipo](../wes/eventmanifestschema-leveltype-complextype.md)complexo de nível.

Os níveis de ETW incluem: 1 crítico; 2 erro; 3 aviso; 4 informações; 5 detalhados.

Com esse erro, o tipo de evento (coluna de tipo) relata "ParseRequestFailed". Nas colunas subsequentes para o evento ParseRequestFailed, vemos uma entrada "InvalidHost". Essa entrada significa que o host identificado na solicitação HTTP está incorreto, de acordo com o protocolo HTTP. Observe que a coluna com a entrada "InvalidHost" não está incluída na tabela para fins de brevidade e para evitar a de colunas não contíguas.

Para corrigir esse problema de análise, o cliente Web deve ser corrigido para estar em conformidade com o RFC HTTP. 

| Nome do evento                    | Tipo               | ID do evento | Versão | Canal | Nível |
|-------------------------------|--------------------|----------|---------|---------|-------|
| EventTrace                    | parâmetro             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | AddUrl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ParseRequestFailed | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | LogFileWrite       | 51       | 0       | 16      | 4     |



 

Tabela 2: trechos de um exemplo de relatório de rastreamento para um problema de análise

 

 