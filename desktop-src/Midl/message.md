---
title: atributo de mensagem
description: O atributo \ Message \ indica que a chamada de procedimento remoto deve ser tratada como uma mensagem do cliente para o servidor.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- MIDL de atributo de mensagem
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454020"
---
# <a name="message-attribute"></a><span data-ttu-id="46af4-104">atributo de mensagem</span><span class="sxs-lookup"><span data-stu-id="46af4-104">message attribute</span></span>

<span data-ttu-id="46af4-105">O atributo **\[ Message \]** indica que a chamada de procedimento remoto deve ser tratada como uma mensagem do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="46af4-105">The **\[message\]** attribute indicates that the remote procedure call is to be treated as a message from the client to the server.</span></span>

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a><span data-ttu-id="46af4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46af4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46af4-107">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="46af4-107">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="46af4-108">Outros atributos que se aplicam à função.</span><span class="sxs-lookup"><span data-stu-id="46af4-108">Other attributes that apply to the function.</span></span> <span data-ttu-id="46af4-109">Somente os **\[** atributos [**local**](local.md) **\]** , **\[** [**Nocode**](nocode.md) **\]** , **\[** [**Code**](code.md)**\]** e **\[** [**Optimize**](optimize.md) **\]** podem ser usados com o atributo **\[ Message \]** .</span><span class="sxs-lookup"><span data-stu-id="46af4-109">Only the **\[**[**local**](local.md)**\]**, **\[**[**nocode**](nocode.md)**\]**, **\[**[**code**](code.md)**\],** and **\[**[**optimize**](optimize.md)**\]** attributes may be used with the **\[message\]** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="46af4-110">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="46af4-110">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="46af4-111">O nome da função, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="46af4-111">The name of the function as defined in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="46af4-112">*atributos de parâmetro opcionais*</span><span class="sxs-lookup"><span data-stu-id="46af4-112">*optional-parameter-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="46af4-113">Zero ou mais atributos MIDL que serão aplicados ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="46af4-113">Zero or more MIDL attributes that will be applied to the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="46af4-114">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="46af4-114">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="46af4-115">O nome do parâmetro, conforme definido no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="46af4-115">The name of the parameter as defined in the IDL file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46af4-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="46af4-116">Remarks</span></span>

<span data-ttu-id="46af4-117">Como mensagens do cliente, as chamadas de procedimento remoto com o atributo **\[ Message \]** são entregues ao servidor de forma assíncrona pelo transporte de enfileiramento de mensagens do [**ncadg \_ MQ**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="46af4-117">As messages from the client, remote procedure calls with the **\[message\]** attribute are delivered to the server asynchronously over the [**ncadg\_mq**](ncadg-mq.md) message-queuing transport.</span></span> <span data-ttu-id="46af4-118">Você pode indicar o sistema de mensagens de modo síncrono especificando o protocolo de transporte **ncadg \_ MQ** sem usar o atributo **\[ \] Message** .</span><span class="sxs-lookup"><span data-stu-id="46af4-118">You can indicate synchronous-mode messaging by specifying the **ncadg\_mq** transport protocol without using the **\[message\]** attribute.</span></span>

<span data-ttu-id="46af4-119">Ao especificar o sistema de mensagens de modo assíncrono, o atributo **\[ Message \]** permite que o cliente faça a chamada de procedimento remoto e retorne imediatamente, mesmo quando o aplicativo do servidor não está respondendo.</span><span class="sxs-lookup"><span data-stu-id="46af4-119">By specifying asynchronous-mode messaging, the **\[message\]** attribute allows the client to make the remote procedure call and return immediately, even when the server application is not responding.</span></span> <span data-ttu-id="46af4-120">Se o servidor de destino não estiver disponível, a chamada será armazenada até que o servidor fique disponível.</span><span class="sxs-lookup"><span data-stu-id="46af4-120">If the target server is not available, the call will be stored until the server becomes available.</span></span>

<span data-ttu-id="46af4-121">Além disso, o sistema de mensagens em modo assíncrono permite controlar as propriedades da fila de recebimento do servidor.</span><span class="sxs-lookup"><span data-stu-id="46af4-121">In addition, asynchronous-mode messaging lets you control message-queue properties of the receive queue for the server.</span></span> <span data-ttu-id="46af4-122">Consulte [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) para obter mais informações sobre como selecionar a qualidade do serviço, a prioridade da chamada e o tempo de vida da chamada para o processo do servidor.</span><span class="sxs-lookup"><span data-stu-id="46af4-122">See [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) for more information on selecting quality of service, call priority, and call lifetime for the server process.</span></span>

<span data-ttu-id="46af4-123">As restrições a seguir também se aplicam ao atributo **\[ Message \]** :</span><span class="sxs-lookup"><span data-stu-id="46af4-123">The following restrictions also apply to the **\[message\]** attribute:</span></span>

-   <span data-ttu-id="46af4-124">O enfileiramento de mensagens da Microsoft deve ser implementado nos sistemas cliente e servidor e os sistemas devem ser visíveis uns aos outros, conforme determinado pelo escopo da instalação da fila de mensagens.</span><span class="sxs-lookup"><span data-stu-id="46af4-124">Microsoft Message Queuing must be implemented in the client and server systems and the systems must be visible to each other as determined by the scope of the message queue installation.</span></span>
-   <span data-ttu-id="46af4-125">A associação deve usar pontos de extremidade bem conhecidos e o protocolo de transporte [**ncadg \_ MQ**](ncadg-mq.md) .</span><span class="sxs-lookup"><span data-stu-id="46af4-125">The binding must use well-known endpoints and the [**ncadg\_mq**](ncadg-mq.md) transport protocol.</span></span>
-   <span data-ttu-id="46af4-126">A função não pode conter parâmetros de saída ou um tipo de retorno diferente de [**void**](void.md).</span><span class="sxs-lookup"><span data-stu-id="46af4-126">The function cannot contain output parameters or a return type other than [**void**](void.md).</span></span> <span data-ttu-id="46af4-127">Observe que a última restrição torna o atributo de **\[ mensagem \]** inadequado para métodos de interface com (Object), neste momento.</span><span class="sxs-lookup"><span data-stu-id="46af4-127">Note that the latter restriction makes the **\[message\]** attribute unsuitable for COM (object) interface methods, at this time.</span></span> <span data-ttu-id="46af4-128">A próxima versão do MIDL permitirá que as funções de **\[ mensagem \]** retornem o status de erro \_ \_ t ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="46af4-128">The next release of MIDL will permit **\[message\]** functions to return error\_status\_t or HRESULT.</span></span>
-   <span data-ttu-id="46af4-129">Qualquer interface que contenha pelo menos uma chamada de **\[ mensagem \]** deve ser registrada chamando [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) antes [**de chamar RpcServerUseProtseqEpEx (ncadg \_ MQ)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span><span class="sxs-lookup"><span data-stu-id="46af4-129">Any interface that contains at least one **\[message\]** call must be registered by calling [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) or [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) before calling [**RpcServerUseProtseqEpEx(ncadg\_mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex).</span></span> <span data-ttu-id="46af4-130">Caso contrário, as chamadas que estavam aguardando na fila para o servidor serão lidas antes da interface ser registrada e as chamadas falharão.</span><span class="sxs-lookup"><span data-stu-id="46af4-130">Otherwise, calls that were waiting on the queue for the server will be read before the interface is registered, and the calls will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="46af4-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="46af4-131">Examples</span></span>

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a><span data-ttu-id="46af4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="46af4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46af4-133">**auto-completar**</span><span class="sxs-lookup"><span data-stu-id="46af4-133">**code**</span></span>](code.md)
</dt> <dt>

[<span data-ttu-id="46af4-134">**local**</span><span class="sxs-lookup"><span data-stu-id="46af4-134">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="46af4-135">**ncadg \_ MQ**</span><span class="sxs-lookup"><span data-stu-id="46af4-135">**ncadg\_mq**</span></span>](ncadg-mq.md)
</dt> <dt>

[<span data-ttu-id="46af4-136">**Nocode**</span><span class="sxs-lookup"><span data-stu-id="46af4-136">**nocode**</span></span>](nocode.md)
</dt> <dt>

[<span data-ttu-id="46af4-137">**formato**</span><span class="sxs-lookup"><span data-stu-id="46af4-137">**optimize**</span></span>](optimize.md)
</dt> <dt>

[<span data-ttu-id="46af4-138">Enfileiramento de mensagens RPC</span><span class="sxs-lookup"><span data-stu-id="46af4-138">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="46af4-139">**RpcBindingSetOption**</span><span class="sxs-lookup"><span data-stu-id="46af4-139">**RpcBindingSetOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[<span data-ttu-id="46af4-140">**RpcBindingInqOption**</span><span class="sxs-lookup"><span data-stu-id="46af4-140">**RpcBindingInqOption**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[<span data-ttu-id="46af4-141">**void**</span><span class="sxs-lookup"><span data-stu-id="46af4-141">**void**</span></span>](void.md)
</dt> </dl>

 

 