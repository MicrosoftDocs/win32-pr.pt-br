---
title: context_handle_serialize atributo
description: O atributo \ Context \_ Handlers \_ SERIALIZE \ ACF garante que um identificador de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo.
ms.assetid: e2f48582-228a-4725-9543-1e638d86ff6b
keywords:
- context_handle_serialize do atributo MIDL
topic_type:
- apiref
api_name:
- context_handle_serialize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74e364c3ae8bf0439e50ae53130542762f37484
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105758783"
---
# <a name="context_handle_serialize-attribute"></a><span data-ttu-id="c9c4b-104">\_ \_ atributo serializar identificador de contexto</span><span class="sxs-lookup"><span data-stu-id="c9c4b-104">context\_handle\_serialize attribute</span></span>

<span data-ttu-id="c9c4b-105">Os **\[ \_ identificadores de contexto \_ serializam \]** o atributo ACF garante que um identificador de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-105">The **\[context\_handle\_serialize\]** ACF attribute guarantees that a context handle will always be serialized, regardless of the application's default behavior.</span></span>

``` syntax
typedef [context_handle_serialize [ , type-acf-attribute-list ] ] context-handle-type;

[context_handle_serialize [, function-acf-attribute-list ] ] function-name( );

function-name(
    [context_handle_serialize [ , parameter-acf-attribute-list ] ] param-name );
```

## <a name="parameters"></a><span data-ttu-id="c9c4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9c4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c4b-107">*tipo-ACF-lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="c9c4b-107">*type-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c4b-108">Quaisquer outros atributos de ACF que se aplicam ao tipo.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-108">Any other ACF attributes that apply to the type.</span></span>

</dd> <dt>

<span data-ttu-id="c9c4b-109">*tipo de identificador de contexto*</span><span class="sxs-lookup"><span data-stu-id="c9c4b-109">*context-handle-type*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c4b-110">O identificador que especifica o tipo de identificador de contexto, conforme definido em uma declaração de [**typedef**](typedef.md) .</span><span class="sxs-lookup"><span data-stu-id="c9c4b-110">The identifier that specifies the context handle type, as defined in a [**typedef**](typedef.md) declaration.</span></span> <span data-ttu-id="c9c4b-111">Esse é o tipo que recebe o atributo de **\[ \_ \_ serialização \] de identificador de contexto** no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-111">This is the type that receives the **\[context\_handle\_serialize\]** attribute in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="c9c4b-112">*função-ACF-atributo-List*</span><span class="sxs-lookup"><span data-stu-id="c9c4b-112">*function-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c4b-113">Quaisquer atributos adicionais do ACF que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-113">Any additional ACF attributes that apply to the function.</span></span>

</dd> <dt>

<span data-ttu-id="c9c4b-114">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="c9c4b-114">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c4b-115">O nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-115">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="c9c4b-116">*parâmetro-ACF-lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="c9c4b-116">*parameter-acf-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c4b-117">Quaisquer outros atributos de ACF que se aplicam ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-117">Any other ACF attributes that apply to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c9c4b-118">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="c9c4b-118">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c9c4b-119">O nome do parâmetro, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-119">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9c4b-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9c4b-120">Remarks</span></span>

<span data-ttu-id="c9c4b-121">O atributo **\[ \_ \_ serializar \] identificador de contexto** identifica um identificador de associação que mantém informações de contexto ou estado no servidor entre chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-121">The **\[context\_handle\_serialize\]** attribute identifies a binding handle that maintains context or state information on the server between remote procedure calls.</span></span> <span data-ttu-id="c9c4b-122">O atributo pode aparecer como um atributo de tipo de [**typedef**](typedef.md) de IDL, como um atributo de tipo de retorno de função ou como um atributo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-122">The attribute can appear as an IDL [**typedef**](typedef.md) type attribute, as a function return type attribute, or as a parameter attribute.</span></span>

<span data-ttu-id="c9c4b-123">Por padrão, as chamadas em identificadores de contexto são serializadas, mas um aplicativo pode chamar [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) para substituir esse comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-123">By default, calls on context handles are serialized, but an application can call [**RpcSsDontSerializeContext**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext) to override this default behavior.</span></span> <span data-ttu-id="c9c4b-124">Usar o atributo de **\[ \_ \_ serialização \] de identificador de contexto** em um arquivo ACF garante que as chamadas nesse identificador de contexto específico serão serializadas, mesmo que o aplicativo de chamada tenha substituído a serialização padrão.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-124">Using the **\[context\_handle\_serialize\]** attribute in an ACF file guarantees that calls on this particular context handle will be serialized, even if the calling application has overridden the default serialization.</span></span> <span data-ttu-id="c9c4b-125">Uma rotina de encerramento de contexto é opcional.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-125">A context rundown routine is optional.</span></span>

<span data-ttu-id="c9c4b-126">Esse atributo está disponível no MIDL versão 5,0.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-126">This attribute is available in MIDL version 5.0.</span></span>

<span data-ttu-id="c9c4b-127">**Windows Server ServerÂ 2003 e WINDOWSÂ XP ou posterior:** Uma única interface pode acomodar identificadores de contexto serializados e não serializados, permitindo que um método em uma interface acesse um identificador de contexto exclusivamente (serializado), enquanto outros métodos acessam esse identificador de contexto no modo compartilhado (não serializado).</span><span class="sxs-lookup"><span data-stu-id="c9c4b-127">**Windows ServerÂ 2003 and WindowsÂ XP or later:** A single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="c9c4b-128">Esses recursos de acesso são comparáveis a mecanismos de bloqueio de leitura/gravação; os métodos que usam um identificador de contexto serializado são usuários exclusivos (gravadores), enquanto os métodos que usam um identificador de contexto não serializado são usuários compartilhados (leitores).</span><span class="sxs-lookup"><span data-stu-id="c9c4b-128">These access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="c9c4b-129">Os métodos que destruim ou modificam o estado de um identificador de contexto devem ser serializados.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-129">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="c9c4b-130">Os métodos que não modificam o estado de um identificador de contexto, como os métodos que simplesmente lêem de um identificador de contexto, podem ser não serializados.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-130">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="c9c4b-131">Observe que os métodos de criação são serializados implicitamente.</span><span class="sxs-lookup"><span data-stu-id="c9c4b-131">Note that creation methods are implicitly serialized.</span></span>

## <a name="examples"></a><span data-ttu-id="c9c4b-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9c4b-132">Examples</span></span>

``` syntax
typedef [context_handle_serialize] PCONTEXT_HANDLE_TYPE; 
HRESULT RemoteFunc([context_handle_serialize] pCxHandle);
```

## <a name="see-also"></a><span data-ttu-id="c9c4b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9c4b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c4b-134">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="c9c4b-134">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="c9c4b-135">Atributos de ACF</span><span class="sxs-lookup"><span data-stu-id="c9c4b-135">ACF Attributes</span></span>](acf-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9c4b-136">**identificador de contexto \_ \_ noserializeize**</span><span class="sxs-lookup"><span data-stu-id="c9c4b-136">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> <dt>

[<span data-ttu-id="c9c4b-137">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="c9c4b-137">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="c9c4b-138">Identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="c9c4b-138">Context Handles</span></span>](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[<span data-ttu-id="c9c4b-139">**RpcSsDontSerializeContext**</span><span class="sxs-lookup"><span data-stu-id="c9c4b-139">**RpcSsDontSerializeContext**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcssdontserializecontext)
</dt> <dt>

[<span data-ttu-id="c9c4b-140">Rotina de execução de contexto de servidor</span><span class="sxs-lookup"><span data-stu-id="c9c4b-140">Server Context Run-down Routine</span></span>](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[<span data-ttu-id="c9c4b-141">Clientes multithread e identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="c9c4b-141">Multithreaded Clients and Context Handles</span></span>](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[<span data-ttu-id="c9c4b-142">**typedef**</span><span class="sxs-lookup"><span data-stu-id="c9c4b-142">**typedef**</span></span>](typedef.md)
</dt> </dl>

 

 