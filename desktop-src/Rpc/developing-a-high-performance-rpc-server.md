---
title: Desenvolvendo um servidor RPC de alto desempenho
description: As informações nesta seção aplicam-se às sequências de protocolo remoto ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np e ao Windows 2000 e Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC de chamada de procedimento remoto, práticas recomendadas, desenvolvimento de um servidor de alto desempenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454283"
---
# <a name="developing-a-high-performance-rpc-server"></a>Desenvolvendo um servidor RPC de alto desempenho

As informações contidas nesta seção aplicam-se a sequências de protocolo remoto: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**NCACN \_ NP**](/windows/desktop/Midl/ncacn-np)e para Windows 2000 e Windows XP.

Esta seção aborda três aspectos principais do desempenho do servidor RPC:

-   [Latência de rede e taxa de transferência](network-latency-and-throughput.md)
-   [Escalabilidade](scalability.md)
-   [Dicas de desempenho de RPC diversas](miscellaneous-rpc-performance-tips.md)

O comprimento do caminho de código é outra consideração de desempenho principal para RPC. O tamanho do caminho de código geralmente é bem compreendido e, como a literatura e as ferramentas estão amplamente disponíveis nesse tópico, este artigo não o resolve.

Uma regra de desempenho geral importante e estabelecida a ser lembrada ao considerar o desempenho de RPC é esta: Encontre o afunilamento no sistema e trabalhe para resolver isso. O afunilamento de retenção pode não ser a programação RPC e, se esse for o caso, o ajuste de desempenho no RPC não resultará em desempenho aprimorado até que o afunilamento seja resolvido. Por exemplo, um sistema afetado pela contenção de recursos não precisa fazer uso mais eficiente da rede.

Se o seu sistema estiver implantado em vários ambientes, é uma boa ideia garantir que todos os aspectos dele sejam bem ajustados, pois diferentes ambientes podem produzir gargalos de desempenho variados.

 

 