---
title: Semântica de falha para alças de contexto
description: Este tópico discute a semântica de falha para os alças de contexto.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9549a659c56c4761de8df4f43c54b823d32f74786af928821ba82b6effc3bba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021266"
---
# <a name="failure-semantics-for-context-handles"></a>Semântica de falha para alças de contexto

Este tópico discute a semântica de falha para os alças de contexto.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Semântica de falha ao fechar o guidão de contexto falha

Imagine um aplicativo cliente está tentando fechar um lidar de contexto aberto no servidor, sem desligar o processo do cliente. Além disso, suponha que a chamada para o servidor para fechar o handle de contexto falhe (por exemplo, o cliente está sem memória). A maneira adequada de lidar com essa situação é chamar a [**função RpcSsDestroyClientContext.**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) Nesse caso, o cliente limpa seu lado do handle de contexto e fecha abortivamente a conexão com o servidor. Como a conexão é, na verdade, um pool de conexões (consulte [RPC](rpc-and-the-network.md)e a Rede ), que é contada com uma referência para cada associação aberta ou alça de contexto, destruir o alçamento de contexto chamando a **função RpcSsDestroyClientContext** não realmente destrói a conexão. Em vez disso, ele diminui a contagem de referência para o pool de conexões. Para que as conexões no pool sejam fechadas, o cliente precisa fechar todos os alças de associação e os alças de contexto para esse servidor do processo do cliente. Em seguida, todas as conexões no pool são fechadas e o mecanismo de run-down do servidor é iniciado e limpo.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Semântica de falha durante a alteração do estado do alça de contexto

As informações nesta seção referem-se Windows XP e plataformas posteriores.

Os alças de contexto são simplesmente parâmetros para uma função. Todas as alterações no estado de um alça de contexto ocorrem quando os parâmetros são empacotados ou não são empacotados. Por exemplo, se um cliente abrir um handle de contexto (altera-o de **NULL** para não **NULL),** o tempo de run-time RPC não abrirá a parte RPC do handle até que os argumentos sejam marshalados para enviar ao cliente. Falhas podem ocorrer durante o intermediário. Devido a uma variedade de possíveis condições de rede ou de recursos baixos, a transmissão do pacote para o cliente pode falhar. Ou a rotina do servidor pode lançar uma exceção ao tentar alterar um alçamento de contexto. Nessas ou em outras situações de falha, o cliente e o servidor podem obter exibições inconsistentes do handle de contexto. Esta seção explica a regra para o estado do handle de contexto e a responsabilidade do código do cliente e do servidor durante várias condições de falha.

-   Um **alça de** contexto NULL chega, mas a rotina do servidor encontra uma falha e lança uma exceção.

    É responsabilidade da rotina do servidor limpar qualquer estado relacionado ao handle de contexto que ele possa ter criado. O tempo de executar RPC limpa seu estado.

-   Um contexto não **NULL** lida com a chegada, mas a rotina do servidor encontra uma falha e lança uma exceção.

    Se a rotina do servidor fechou o handle de contexto, o cliente não o conhecerá, pois a chamada não terá êxito; O uso posterior do alça de contexto resultará em um erro RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH no cliente. Se a rotina do servidor não modificar o handle de contexto, o cliente ainda poderá usá-lo. Se a rotina do servidor mudar as informações armazenadas no contexto do servidor, novas chamadas do cliente usarão essas informações.

-   Um alça de contexto não **NULL** chega e a rotina do servidor fecha o alçamento, mas o marshaling após o marshaling do handle de contexto falhou ou o processamento após a falha do marshaling.

    O handle de contexto é fechado e chamadas posteriores por esse cliente usando esse handle de contexto resultam em um erro RPC \_ X \_ SS \_ CONTEXT \_ MISMATCH no cliente.

-   Um **handle de** contexto NULL chega e o servidor cria seu contexto para esse manipular, mas marshaling após a falha do marshaling do handle de contexto ou processamento após a falha do marshaling.

    Nesse caso, o tempo de run time de RPC invoca o run down para esse handle de contexto e limpa o estado RPC para esse handle de contexto. O alça de contexto não será criado no lado do cliente.

-   Um alça de contexto não **NULL** chega e o servidor não altera o alçamento de contexto ou altera as informações armazenadas no contexto do servidor e o marshaling falha após o marshaling do handle de contexto.

    Novas chamadas do cliente usarão o alça de contexto que o servidor tem.

-   Um **alça de** contexto NULL chega e o servidor não o configura como nada diferente de **NULL,** mas a chamada falha antes que o alça de contexto seja marshalado.

    Nesse caso, nenhum alça de contexto é criado no cliente.

-   Um alça de **contexto não NULL** chega e o servidor o define como **NULL,** mas o marshaling falha antes que o handle de contexto seja marshaling.

    Nesse caso, o handle de contexto permanece fechado no servidor e o cliente obtém erros de INCOMPATIBILIDADE DE CONTEXTO RPC X SS quando tenta usar o alça \_ \_ de \_ \_ contexto.

-   Um **alça de** contexto NULL chega ao servidor e o servidor o define como não **NULL,** mas o marshaling falha antes que o handle de contexto seja marshaling.

    O run down do alça de contexto deve ser invocado para que o servidor possa ser limpo e nenhum alça de contexto será criado no cliente.

-   Um alça de contexto não **NULL** chega e o servidor não altera o alçamento de contexto ou altera as informações armazenadas no contexto do servidor e o marshaling falha antes que o handle de contexto seja marshalado.

    Novas chamadas do cliente usarão o estado no servidor.

-   Um alça de contexto é declarado como um valor de retorno e a rotina do servidor retorna **NULL** para o handle de contexto e o marshaling falha antes que o handle de contexto seja marshaling.

    Nesse caso, nenhum novo contexto é criado no cliente.

-   Um alça de contexto é declarado como um valor de retorno e a rotina do servidor retorna não **NULL** para o handle de contexto e o marshaling falha antes que o handle de contexto seja marshaling.

    O tempo de executar RPC chama a rotina de run-down do alça de contexto para dar a ela a oportunidade de limpar e nenhum novo contexto é criado no cliente.

 

 




