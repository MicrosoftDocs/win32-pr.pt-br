---
title: Serialização de modo misto de identificadores de contexto
description: no Microsoft Windows XP, uma única interface pode acomodar identificadores de contexto serializados e não serializados, que é chamado de serialização de modo misto.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MIDL de referência de linguagem MIDL, serialização de modo misto de identificadores de contexto
- identificadores de contexto MIDL
- MIDL de serialização de modo misto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aaa35f02a939a50e2484ace29630783ee219d6313d7538cba54b1f54cd83007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787426"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serialização de modo misto de identificadores de contexto

a partir do Windows XP, uma única interface pode acomodar identificadores de contexto serializados e não serializados, permitindo que um método em uma interface acesse um identificador de contexto exclusivamente (serializado), enquanto outros métodos acessam esse identificador de contexto no modo compartilhado (não serializado). Para obter mais informações sobre identificadores de contexto, consulte os seguintes atributos:

-   [**identificador de contexto \_**](context-handle.md)
-   [**\_serializar identificador de contexto \_**](context-handle-serialize.md)
-   [**identificador de contexto \_ \_ noserializeize**](context-handle-noserialize.md)

Os recursos de acesso em modo serializado e compartilhado são comparáveis aos mecanismos de bloqueio de leitura/gravação; os métodos que usam um identificador de contexto serializado são usuários exclusivos (gravadores), enquanto os métodos que usam um identificador de contexto não serializado são usuários compartilhados (leitores). Os métodos que destruim ou modificam o estado de um identificador de contexto devem ser serializados. Os métodos que não modificam o estado de um identificador de contexto, como os métodos que simplesmente lêem de um identificador de contexto, podem ser não serializados. O uso de um identificador de contexto no modo misto pode melhorar substancialmente a escalabilidade de um servidor, especialmente quando vários threads fazem chamadas simultâneas para o mesmo identificador de contexto.

O RPC não impõe "bloqueio de gravação" em métodos que usam um identificador de contexto no modo compartilhado, o que significa que os aplicativos devem garantir que os identificadores de contexto de modo compartilhado não sejam modificados. A modificação de um identificador de contexto usado no modo compartilhado pode resultar em danos sutis de conteúdo de identificador de contexto, que são impossíveis de depurar.

Alterar a lógica de serialização de um identificador de contexto afeta apenas o servidor. Além disso, a alteração da lógica de serialização de um identificador de contexto não afeta o formato de conexão e, portanto, as alterações na lógica de serialização em um servidor não afetam a capacidade dos clientes existentes de interagir com o servidor.

Não é recomendável usar apenas identificadores de contexto não serializados. Os servidores que usam identificadores não serializados devem mudar para o acesso serializado para o método que fecha o identificador de contexto.

Identificadores de contexto que são \[ \] normalmente são usados por métodos de criação e não exigem serialização. Portanto, qualquer atributo de serialização aplicado \[ a \] identificadores de contexto somente de saída, como [**\_ \_ serialização de identificador de contexto**](context-handle-serialize.md) ou identificador de [**contexto \_ \_ noserializate**](context-handle-noserialize.md), é ignorado por RPC.

> [!Note]  
> Os métodos de criação são serializados implicitamente.

 

## <a name="examples"></a>Exemplos

Os dois exemplos a seguir mostram como habilitar a serialização de modo misto de identificadores de contexto.

O primeiro exemplo mostra como fazer isso no arquivo IDL:

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

O segundo exemplo mostra como habilitar a serialização de modo misto de identificadores de contexto no arquivo ACF:

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**identificador de contexto \_**](context-handle.md)
</dt> <dt>

[**\_serializar identificador de contexto \_**](context-handle-serialize.md)
</dt> <dt>

[**identificador de contexto \_ \_ noserializeize**](context-handle-noserialize.md)
</dt> </dl>

 

 




