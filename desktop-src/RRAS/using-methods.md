---
title: Usando métodos
description: Quando um cliente se registra no gerenciador de tabelas de roteamento, ele pode exportar um conjunto de métodos. Esses métodos são usados por outros clientes para obter informações específicas do cliente. Os métodos permitem a comunicação privada entre clientes do gerenciador de tabelas de roteamento.
ms.assetid: 6d984a02-d005-43ad-81c4-968ae9c1a105
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150edb6435e0021c13e129f7c1e7a3016dc0974283fcdd138189f7d1c4a3184a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025096"
---
# <a name="using-methods"></a>Usando métodos

Quando um cliente se registra no gerenciador de tabelas de roteamento, ele pode exportar um conjunto de métodos. Esses métodos são usados por outros clientes para obter informações específicas do cliente. Os métodos permitem a comunicação privada entre clientes do gerenciador de tabelas de roteamento.

Um cliente pode obter a lista de métodos exportados por outro cliente. O cliente chama a [**função RtmGetEntityMethods,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentitymethods) fornecendo o handle do cliente de destino.

Cada método exportado por um cliente é identificado exclusivamente por seu identificador de método. Cada cliente pode exportar até 32 métodos. Cada método corresponde a um bit definido no **membro MethodType** da estrutura [**RTM \_ ENTITY EXPORT \_ \_ METHOD.**](/windows/win32/api/rtmv2/nc-rtmv2-_entity_method) Para invocar vários métodos, o cliente deve executar um OR lógico dos identificadores para esses métodos. A sintaxe e a semântica das estruturas de entrada e saída para cada protocolo devem ser especificadas quando o protocolo é implementado.

> [!Note]  
> Os valores de identificador de método que correspondem a um bit definido na metade inferior do membro **MethodType** (os 16 bits inferiores) são reservados pela Microsoft.

 

Para invocar o método de um segundo cliente, um cliente chama a [**função RtmInvokeMethod.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) O gerenciador de tabela de roteamento descarriza todas as solicitações para invocar os métodos de um cliente. O gerenciador de tabelas de roteamento executa duas funções quando ele é reencontrado entre clientes:

-   Impedir que o segundo cliente invocar um método para um cliente que não está sendo registro.
-   Mantendo uma solicitação de "invocação" quando os métodos são bloqueados e permitindo que a solicitação continue quando os métodos são desbloqueados.

Se um cliente deve impedir que outros clientes executam seus métodos, o cliente pode chamar [**RtmBlockMethods**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmblockmethods). O gerenciador de tabela de roteamento não permitirá que uma chamada para [**RtmInvokeMethod**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminvokemethod) seja processada até que o cliente desbloqueie seus métodos novamente.

Os clientes normalmente bloqueiam métodos ao fazer alterações nos dados privados que são trocados entre clientes. Os métodos de bloqueio são uma ação opcional. Um cliente também pode usar bloqueios internos para impedir que outros clientes invocarem métodos.

Para obter um código de exemplo que mostra como usar essas funções, consulte Obter e chamar [os métodos exportados para um cliente](obtain-and-call-the-exported-methods-for-a-client.md).

 

 




