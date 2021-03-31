---
title: Serialização de modo misto de identificadores de contexto
description: No Microsoft Windows XP, uma única interface pode acomodar identificadores de contexto serializados e não serializados, que é chamado de serialização de modo misto.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MIDL de referência de linguagem MIDL, serialização de modo misto de identificadores de contexto
- identificadores de contexto MIDL
- MIDL de serialização de modo misto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822598"
---
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="2f2e8-106">Serialização de modo misto de identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="2f2e8-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="2f2e8-107">A partir do Windows XP, uma única interface pode acomodar identificadores de contexto serializados e não serializados, permitindo que um método em uma interface acesse um identificador de contexto exclusivamente (serializado), enquanto outros métodos acessam esse identificador de contexto no modo compartilhado (não serializado).</span><span class="sxs-lookup"><span data-stu-id="2f2e8-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="2f2e8-108">Para obter mais informações sobre identificadores de contexto, consulte os seguintes atributos:</span><span class="sxs-lookup"><span data-stu-id="2f2e8-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="2f2e8-109">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="2f2e8-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="2f2e8-110">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="2f2e8-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="2f2e8-111">**identificador de contexto \_ \_ noserializeize**</span><span class="sxs-lookup"><span data-stu-id="2f2e8-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="2f2e8-112">Os recursos de acesso em modo serializado e compartilhado são comparáveis aos mecanismos de bloqueio de leitura/gravação; os métodos que usam um identificador de contexto serializado são usuários exclusivos (gravadores), enquanto os métodos que usam um identificador de contexto não serializado são usuários compartilhados (leitores).</span><span class="sxs-lookup"><span data-stu-id="2f2e8-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="2f2e8-113">Os métodos que destruim ou modificam o estado de um identificador de contexto devem ser serializados.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="2f2e8-114">Os métodos que não modificam o estado de um identificador de contexto, como os métodos que simplesmente lêem de um identificador de contexto, podem ser não serializados.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="2f2e8-115">O uso de um identificador de contexto no modo misto pode melhorar substancialmente a escalabilidade de um servidor, especialmente quando vários threads fazem chamadas simultâneas para o mesmo identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="2f2e8-116">O RPC não impõe "bloqueio de gravação" em métodos que usam um identificador de contexto no modo compartilhado, o que significa que os aplicativos devem garantir que os identificadores de contexto de modo compartilhado não sejam modificados.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="2f2e8-117">A modificação de um identificador de contexto usado no modo compartilhado pode resultar em danos sutis de conteúdo de identificador de contexto, que são impossíveis de depurar.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="2f2e8-118">Alterar a lógica de serialização de um identificador de contexto afeta apenas o servidor.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="2f2e8-119">Além disso, a alteração da lógica de serialização de um identificador de contexto não afeta o formato de conexão e, portanto, as alterações na lógica de serialização em um servidor não afetam a capacidade dos clientes existentes de interagir com o servidor.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="2f2e8-120">Não é recomendável usar apenas identificadores de contexto não serializados.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="2f2e8-121">Os servidores que usam identificadores não serializados devem mudar para o acesso serializado para o método que fecha o identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="2f2e8-122">Identificadores de contexto que são \[ \] normalmente são usados por métodos de criação e não exigem serialização.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="2f2e8-123">Portanto, qualquer atributo de serialização aplicado \[ a \] identificadores de contexto somente de saída, como [**\_ \_ serialização de identificador de contexto**](context-handle-serialize.md) ou identificador de [**contexto \_ \_ noserializate**](context-handle-noserialize.md), é ignorado por RPC.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="2f2e8-124">Os métodos de criação são serializados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2f2e8-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2f2e8-125">Examples</span></span>

<span data-ttu-id="2f2e8-126">Os dois exemplos a seguir mostram como habilitar a serialização de modo misto de identificadores de contexto.</span><span class="sxs-lookup"><span data-stu-id="2f2e8-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="2f2e8-127">O primeiro exemplo mostra como fazer isso no arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="2f2e8-127">The first example shows how to do so in the IDL file:</span></span>

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

<span data-ttu-id="2f2e8-128">O segundo exemplo mostra como habilitar a serialização de modo misto de identificadores de contexto no arquivo ACF:</span><span class="sxs-lookup"><span data-stu-id="2f2e8-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="2f2e8-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f2e8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f2e8-130">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="2f2e8-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="2f2e8-131">**\_serializar identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="2f2e8-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="2f2e8-132">**identificador de contexto \_ \_ noserializeize**</span><span class="sxs-lookup"><span data-stu-id="2f2e8-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




