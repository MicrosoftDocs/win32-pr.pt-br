---
title: Usando métodos
description: Quando um cliente é registrado com o Gerenciador de tabela de roteamento, ele pode exportar um conjunto de métodos. Esses métodos são usados por outros clientes para obter informações específicas do cliente. Os métodos permitem a comunicação privada entre clientes do Gerenciador de tabela de roteamento.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd895fbb3f8f54224522786b5794c5c6c57a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916353"
---
# <a name="using-methods"></a>Usando métodos

Quando um cliente é registrado com o Gerenciador de tabela de roteamento, ele pode exportar um conjunto de métodos. Esses métodos são usados por outros clientes para obter informações específicas do cliente. Os métodos permitem a comunicação privada entre clientes do Gerenciador de tabela de roteamento.

Um cliente pode obter a lista de métodos exportados por outro cliente. O cliente chama a função [**RtmGetEntityMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) , fornecendo o identificador do cliente de destino.

Cada método exportado por um cliente é identificado exclusivamente por seu identificador de método. Cada cliente pode exportar até 32 métodos. Cada método corresponde a um conjunto de bits no membro **MethodType** da estrutura [**do \_ \_ \_ método de exportação da entidade RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) . Para invocar vários métodos, o cliente deve executar uma lógica ou dos identificadores para esses métodos. A sintaxe e a semântica de estruturas de entrada e saída para cada protocolo devem ser especificadas quando o protocolo é implementado.

> [!Note]  
> Os valores de identificador de método que correspondem a um conjunto de bits na metade inferior do membro **MethodType** (os 16 bits inferiores) são reservados pela Microsoft.

 

Para invocar um segundo método de cliente, um cliente chama a função [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) . O Gerenciador de tabela de roteamento arbitra todas as solicitações para invocar os métodos de um cliente. O Gerenciador de tabela de roteamento executa duas funções quando arbitra entre clientes:

-   Impedir que o segundo cliente invoque um método para um cliente que está cancelando o registro.
-   Manter uma solicitação "Invoke" quando os métodos são bloqueados e permitir que a solicitação continue quando os métodos são desbloqueados.

Se um cliente precisar impedir que outros clientes executem seus métodos, o cliente poderá chamar [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods). O Gerenciador de tabela de roteamento não permitirá que uma chamada para [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) seja processada até que o cliente desbloqueie seus métodos novamente.

Os clientes normalmente bloqueiam métodos ao fazer alterações nos dados privados trocados entre clientes. Os métodos de bloqueio são uma ação opcional. Um cliente também pode usar bloqueios internos para impedir que outros clientes invoquem métodos.

Para obter um exemplo de código que mostra como usar essas funções, consulte [obter e chamar os métodos exportados para um cliente](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




