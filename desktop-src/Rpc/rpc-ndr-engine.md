---
title: Mecanismo de NDR de RPC (RPC)
description: O mecanismo de representação de dados de rede (NDR) da chamada de procedimento remoto (RPC) é o mecanismo de marshaling dos componentes RPC e DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bf7ba92a74d2d7dc8c394c561f65337db13af99
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008724"
---
# <a name="rpc-ndr-engine-rpc"></a>Mecanismo de NDR de RPC (RPC)

O mecanismo de representação de dados de rede (NDR) da chamada de procedimento remoto (RPC) é o mecanismo de marshaling dos componentes RPC e DCOM. O mecanismo de NDR lida com todos os problemas relacionados a stub de uma chamada remota. Como um processo, o marshaling de NDR é controlado pelo código C de stubs gerados por MIDL, um gerador de tipo JIT de MIDL ou por stubs gerados por outras ferramentas ou gravados manualmente. Por sua vez, o mecanismo de NDR orienta o tempo de execução subjacente (DCOM ou RPC) que se comunica com transportes específicos.

Embora os stubs sejam código C que são gerados pelo MIDL, os aplicativos são aconselhados a tratar stubs como opacos e altamente desencorajados de modificar qualquer coisa dentro do stub. O comportamento será indefinido se essas rotinas de NDR forem chamadas fora do contexto.

O mecanismo NDR de RPC é descrito mais detalhadamente nos seguintes tópicos:

-   [Sintaxe de transferência e NDR64](transfer-syntax-and-ndr64.md)
-   [Cadeias de caracteres de formato NDR de RPC](rpc-ndr-format-strings.md)
-   [Referência da interface NDR de RPC](rpc-ndr-interface-reference.md)

 

 




