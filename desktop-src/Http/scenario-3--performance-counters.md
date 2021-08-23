---
title: Cenário 3 contadores de desempenho
description: Os contadores de desempenho medem quantidades de informações ou dados, de acordo com o número, o tamanho, a duração e a taxa de dados que estão sendo solicitados ou recebidos.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92afacf959c72735adea25c3ace60c8ae032da66394dda6731fdab913407e21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950715"
---
# <a name="scenario-3-performance-counters"></a>Cenário 3: contadores de desempenho

Os contadores de desempenho medem quantidades de informações ou dados, de acordo com o número, o tamanho, a duração e a taxa de dados que estão sendo solicitados ou recebidos. Você não deve esperar obter uma lista de detalhes de um contador, como uma lista de mensagens de erro. Em vez disso, use contadores de desempenho para obter quantidades, como o número de mensagens de erro desde a inicialização ou a taxa na qual as mensagens de erro estão sendo geradas.

## <a name="performance-counters-for-httpsys"></a>Contadores de desempenho para HTTP.sys

a partir do Windows Vista e do Windows Server 2008, o HTTP.sys tem os seguintes contadores de métrica de desempenho para ajudá-lo com monitoramento, diagnóstico e planejamento de capacidade para servidores web: o componente de API do servidor HTTP tem os seguintes contadores de desempenho para ajudá-lo com monitoramento, diagnóstico e planejamento de capacidade para servidores web:

- Contadores de serviço HTTP:
  - Número de URIs no cache, adicionadas desde a inicialização, excluídas desde a inicialização e o número de liberações de cache
  - Acertos de cache/segundo e erros de cache/segundo
- Grupos de URLs de serviço HTTP:
  - Taxa de envio de dados, taxa de recebimento de dados, bytes transferidos (enviados e recebidos)
  - Número máximo de conexões, taxa de tentativas de conexão, taxa para solicitações GET e HEAD e número total de solicitações
- Filas de solicitação de serviço HTTP:
  - Número de solicitações na fila, idade das solicitações mais antigas na fila (idade da última solicitação na fila)
  - Taxa de entradas de solicitação na fila, taxa de rejeição, número total de solicitações rejeitadas, taxa de acertos de cache

**Acessando contadores de desempenho**

1.  Digite **Perfmon** no prompt de comando para iniciar o console de diagnóstico de desempenho.
2.  Selecione **Monitor de desempenho** no controle de árvore e, em seguida, abra **Adicionar contadores** clicando em **+** .
3.  Em **Adicionar contadores** , selecione entre os três conjuntos de contadores de desempenho: **serviço http**, **filas de solicitação de serviço http** ou **grupos de URL de serviço http**.
4.  Para exibir os contadores dos conjuntos de contadores **filas de solicitação de serviço http** e **grupos de URLs de serviço http** , selecione **instâncias** e clique em **Adicionar** e, em seguida, clique em **OK**. Para exibir os contadores de serviço HTTP, selecione o conjunto de contadores no painel esquerdo e clique em **Adicionar**.

> [!Note]  
> Há apenas uma instância dos contadores da API do servidor HTTP por computador, pois esses contadores representam o estado de todo o componente. Com instâncias de contadores de desempenho do grupo de URLs, a ID da instância (para o contador de desempenho) corresponderá à ID do grupo de URLs. A ID do grupo de URLs pode ser exibida executando **netsh http show ServiceState**. Com instâncias de contadores de desempenho de filas de solicitações, o nome da instância corresponde ao nome da fila de solicitações. O nome da fila de solicitação (se houver) pode ser mostrado pelo mesmo **netsh http show ServiceState**. No entanto, alguns aplicativos de servidor podem ter filas de solicitação sem nome que não podem corresponder a uma ID de instância de contador de desempenho.

 

 

 




