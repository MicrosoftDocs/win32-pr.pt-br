---
title: Semântica de falha para identificadores de contexto
description: Este tópico discute a semântica de falha para identificadores de contexto.
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4528b3f5160b92a4e6f10dbcf877e9fec59f81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005581"
---
# <a name="failure-semantics-for-context-handles"></a>Semântica de falha para identificadores de contexto

Este tópico discute a semântica de falha para identificadores de contexto.

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a>Falha na semântica ao fechar o identificador de contexto

Imagine que um aplicativo cliente está tentando fechar um identificador de contexto aberto no servidor, sem desligar o processo do cliente. Além disso, suponha que a chamada para o servidor feche o identificador de contexto falha (por exemplo, o cliente está sem memória). A maneira apropriada de lidar com essa situação é chamar a função [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) . Nesse caso, o cliente limpa seu lado do identificador de contexto e abortively fecha a conexão com o servidor. Como a conexão é realmente um pool de conexões (Confira [RPC e a rede](rpc-and-the-network.md)), que é contado por referência com uma referência para cada associação aberta ou identificador de contexto, a destruição do identificador de contexto chamando a função **RpcSsDestroyClientContext** não destrói realmente a conexão. Em vez disso, reduz a contagem de referência para o pool de conexões. Para que as conexões no pool sejam fechadas, o cliente precisa fechar todos os identificadores de associação e identificadores de contexto para esse servidor a partir do processo do cliente. Em seguida, todas as conexões no pool são fechadas e o mecanismo de execução do servidor é iniciado e apagado.

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a>Semântica de falha durante a alteração do estado do identificador de contexto

As informações contidas nesta seção referem-se ao Windows XP e às plataformas posteriores.

Os identificadores de contexto são simplesmente parâmetros para uma função. Todas as alterações no estado de um identificador de contexto ocorrem quando os parâmetros são empacotados ou não são empacotados. Por exemplo, se um cliente abrir um identificador de contexto (altera-o de **nulo** para não **nulo**), o tempo de execução de RPC não abrirá realmente a parte RPC do identificador até que os argumentos sejam empacotados para envio ao cliente. As falhas podem ocorrer durante o interim. Devido a uma grande quantidade de condições de rede ou de poucos recursos possíveis, a transmissão do pacote para o cliente pode falhar. Ou a rotina de servidor pode lançar uma exceção ao tentar alterar um identificador de contexto. Nessas ou em outras situações de falha, o cliente e o servidor podem obter exibições inconsistentes do identificador de contexto. Esta seção explica a regra para o estado do identificador de contexto e a responsabilidade do código do cliente e do servidor durante várias condições de falha.

-   Um identificador de contexto **nulo** chega, mas a rotina de servidor encontra uma falha e gera uma exceção.

    É responsabilidade da rotina do servidor de limpar qualquer estado relacionado ao identificador de contexto que possa ter criado. O tempo de execução de RPC limpa seu estado.

-   Um identificador de contexto não **nulo** chega, mas a rotina de servidor encontra uma falha e gera uma exceção.

    Se a rotina de servidor fechou o identificador de contexto, o cliente não saberá, pois a chamada não terá sucesso; o uso adicional do identificador de contexto resultará em um \_ erro de incompatibilidade de contexto de RPC X \_ SS \_ \_ no cliente. Se a rotina de servidor não modificar o identificador de contexto, o cliente ainda poderá usá-lo. Se a rotina de servidor alterar as informações armazenadas no contexto do servidor, novas chamadas do cliente usarão essas informações.

-   Um identificador de contexto não **nulo** chega e a rotina de servidor fecha o identificador, mas o marshaling após o marshaling do identificador de contexto falhou ou o processamento após o marshaling falhou.

    O identificador de contexto é fechado e chamadas adicionais por esse cliente usando esse identificador de contexto resultam em um \_ erro de incompatibilidade de contexto de RPC X \_ SS \_ \_ no cliente.

-   Um identificador de contexto **nulo** chega e o servidor cria seu contexto para esse identificador, mas o marshaling após o marshaling do identificador de contexto falhou ou o processamento após o marshaling falhou.

    Nesse caso, o tempo de execução RPC invoca a execução para esse identificador de contexto e limpa o estado RPC para esse identificador de contexto. O identificador de contexto não será criado no lado do cliente.

-   Um identificador de contexto não **nulo** chega e o servidor não altera o identificador de contexto ou altera as informações armazenadas no contexto do servidor e o marshaling falha depois que o identificador de contexto é empacotado.

    Novas chamadas do cliente usarão o identificador de contexto que o servidor tem.

-   Um identificador de contexto **nulo** chega e o servidor não o define como algo diferente de **NULL**, mas a chamada falha antes que o identificador de contexto seja empacotado.

    Nesse caso, nenhum identificador de contexto é criado no cliente.

-   Um identificador de contexto não **nulo** chega e o servidor o define como **nulo**, mas o marshaling falha antes que o identificador de contexto seja empacotado.

    Nesse caso, o identificador de contexto permanece fechado no servidor e o cliente obtém \_ erros de incompatibilidade de contexto de RPC X \_ SS \_ \_ ao tentar usar o identificador de contexto.

-   Um identificador de contexto **nulo** chega ao servidor e o servidor o define como não **nulo**, mas o marshaling falha antes que o identificador de contexto seja empacotado.

    A execução do identificador de contexto é invocada para que o servidor possa ser limpo e nenhum identificador de contexto será criado no cliente.

-   Um identificador de contexto não **nulo** chega e o servidor não altera o identificador de contexto ou altera as informações armazenadas no contexto do servidor e o marshaling falha antes que o identificador de contexto seja empacotado.

    Novas chamadas do cliente usarão o estado no servidor.

-   Um identificador de contexto é declarado como um valor de retorno e a rotina de servidor retorna **NULL** para o identificador de contexto e o marshaling falha antes que o identificador de contexto seja empacotado.

    Nesse caso, nenhum contexto novo é criado no cliente.

-   Um identificador de contexto é declarado como um valor de retorno, e a rotina de servidor retorna um não **nulo** para o identificador de contexto e o marshaling falha antes que o identificador de contexto seja empacotado.

    O tempo de execução RPC chama a rotina de execução do manipulador de contexto para dar a ela a oportunidade de limpar e nenhum contexto novo é criado no cliente.

 

 




