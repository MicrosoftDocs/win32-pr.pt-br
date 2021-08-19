---
title: Desenvolvendo um servidor RPC de alto desempenho
description: As informações nesta seção se aplica às sequências de protocolo remoto ncacn \_ ip \_ tcp, ncacn http, ncacn np e ao \_ Windows \_ 2000 e Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC de Chamada de Procedimento Remoto , melhores práticas, desenvolvendo um servidor de alto desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c52587410b10ae17f2ebd858863327aaf5ab1def92600259c8e49edc87946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021762"
---
# <a name="developing-a-high-performance-rpc-server"></a>Desenvolvendo um servidor RPC de alto desempenho

As informações nesta seção se aplica a sequências de protocolo remoto: [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)e para Windows 2000 e Windows XP.

Esta seção aborda três aspectos principais do desempenho do servidor RPC:

-   [Latência de rede e produtividade](network-latency-and-throughput.md)
-   [Escalabilidade](scalability.md)
-   [Desempenho diverso de RPC Dicas](miscellaneous-rpc-performance-tips.md)

O comprimento do caminho do código é outra consideração de desempenho principal para RPC. O comprimento do caminho do código geralmente é bem compreendido e, como a escrita e as ferramentas estão amplamente disponíveis nesse tópico, este artigo não aborda isso.

Uma regra de desempenho geral importante e estabelecida a ser lembrada ao considerar o desempenho de RPC é esta: encontrar o gargalo no sistema e trabalhar para resolver isso. O gargalo de gating pode não ser a programação RPC e, se esse for o caso, o ajuste de desempenho no RPC não resultará em desempenho aprimorado até que esse gargalo seja resolvido. Por exemplo, um sistema com contenção de recursos não precisa fazer uso mais eficiente da rede.

Se o sistema for implantado em vários ambientes, é uma boa ideia garantir que todos os aspectos dele sejam bem ajustados, pois ambientes diferentes podem produzir gargalos de desempenho variados.

 

 