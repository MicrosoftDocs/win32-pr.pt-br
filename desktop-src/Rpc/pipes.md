---
title: Pipes (RPC)
description: O construtor de tipo de pipe é um mecanismo altamente eficiente para passar grandes quantidades de dados ou qualquer quantidade de dados que não estão todos disponíveis na memória ao mesmo tempo.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC de Chamada de Procedimento Remoto , descrito, pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c477dc249e400022efda21fef4055840c5095e74500f4ae0bea375310b1903f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927518"
---
# <a name="pipes-rpc"></a>Pipes (RPC)

O construtor de tipo de pipe é um mecanismo altamente eficiente para passar grandes quantidades de dados ou qualquer quantidade de dados que não estão todos disponíveis na memória ao mesmo tempo. Usando um pipe, o tempo de executar RPC lida com a transferência de dados real, eliminando a sobrecarga associada a chamadas de procedimento remoto repetidas.

Depois que um cliente invoca um procedimento remoto que tem um parâmetro de pipe, o cliente e o servidor entram em loops para transferir dados. Os dados podem ser produzidos no cliente ou no servidor. De qualquer forma, a quantidade de dados (em bytes) não precisa ser conhecida com antecedência. Os dados podem ser produzidos ou consumidos incrementalmente. Enquanto estiver no loop de transferência de dados, o servidor chama rotinas de stub que carregam ou descarregam um buffer de dados. O cliente chama procedimentos definidos pelo programador para alocar buffers, carregar dados e descarregar dados dos buffers.

Esta seção fornece uma visão geral do uso de pipes para chamadas de procedimento remoto. Ele apresenta a visão geral nos tópicos a seguir:

-   [Terminologia de pipe essencial](essential-pipe-terminology.md)
-   [O estado do pipe](the-pipe-state.md)
-   [Definindo pipes em arquivos IDL](defining-pipes-in-idl-files.md)
-   [Implementação de pipe do lado do cliente](client-side-pipe-implementation.md)
-   [Implementação de pipe do lado do servidor](server-side-pipe-implementation.md)
-   [Regras para vários pipes](rules-for-multiple-pipes.md)
-   [Combinando parâmetros pipe e nonpipe](combining-pipe-and-nonpipe-parameters.md)

Para obter mais informações sobre sintaxe e restrições de [pipe, consulte pipe](/windows/desktop/Midl/pipe) na Referência de linguagem MIDL. O programa de exemplo PIPES no diretório rpc de exemplos do SDK (Platform Software Development Kit) demonstra como usar pipes \\ **\[ in,out \]** para transferir dados entre um cliente e um servidor.

 

 
