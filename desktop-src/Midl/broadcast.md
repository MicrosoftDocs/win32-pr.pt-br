---
title: atributo de difusão
description: A palavra-chave \ Broadcast \ especifica que as chamadas de procedimento remoto sejam enviadas a todos os servidores em uma rede local.
ms.assetid: 3951c80f-b7f1-457b-9eee-6e075291b27e
keywords:
- MIDL do atributo de difusão
topic_type:
- apiref
api_name:
- broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c2bbb724fc292a5e3942bf2b6de61b5631cdc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293297"
---
# <a name="broadcast-attribute"></a><span data-ttu-id="7bfa6-104">atributo de difusão</span><span class="sxs-lookup"><span data-stu-id="7bfa6-104">broadcast attribute</span></span>

<span data-ttu-id="7bfa6-105">A **\[ difusão \]** de palavra-chave especifica que as chamadas de procedimento remoto sejam enviadas a todos os servidores em uma rede local.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-105">The keyword **\[broadcast\]** specifies that remote procedure calls be sent to all servers on a local network.</span></span>

``` syntax
[
    interface-attribute-list
] 
interface interface-name 
{
    [broadcast [, attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a><span data-ttu-id="7bfa6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bfa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bfa6-107">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="7bfa6-107">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfa6-108">Especifica uma lista de zero ou mais atributos IDL que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-108">Specifies a list of zero or more IDL attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="7bfa6-109">Quando dois ou mais atributos de interface estão presentes, eles devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-109">When two or more interface attributes are present, they must be separated by commas.</span></span>

</dd> <dt>

<span data-ttu-id="7bfa6-110">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="7bfa6-110">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfa6-111">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-111">Specifies the name of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="7bfa6-112">*lista de atributos*</span><span class="sxs-lookup"><span data-stu-id="7bfa6-112">*attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfa6-113">Especifica atributos adicionais a serem aplicados à função.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-113">Specifies additional attributes to be applied to the function.</span></span> <span data-ttu-id="7bfa6-114">Separe vários atributos com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-114">Separate multiple attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="7bfa6-115">*ReturnType*</span><span class="sxs-lookup"><span data-stu-id="7bfa6-115">*returntype*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfa6-116">Especifica o tipo de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-116">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="7bfa6-117">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="7bfa6-117">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfa6-118">Especifica o nome da função à qual o atributo de **\[ difusão \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-118">Specifies the name of the function to which the **\[broadcast\]** attribute will be applied.</span></span>

</dd> <dt>

<span data-ttu-id="7bfa6-119">*params*</span><span class="sxs-lookup"><span data-stu-id="7bfa6-119">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfa6-120">Lista de parâmetros de função.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-120">Function parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7bfa6-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bfa6-121">Remarks</span></span>

<span data-ttu-id="7bfa6-122">A palavra-chave **\[ Broadcast \]** especifica que a rotina sempre é transmitida para todos os servidores na rede, em vez de ser entregue a um servidor específico. O cliente recebe a saída da primeira resposta a ser retornada com êxito, enquanto as respostas subsequentes são descartadas.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-122">The **\[broadcast\]** keyword specifies that the routine is always broadcasted to all the servers on the network, rather than being delivered to one particular server.The client receives output from the first reply to return successfully, while subsequent replies are discarded.</span></span>

<span data-ttu-id="7bfa6-123">Uma operação com o atributo **\[ Broadcast \]** é implicitamente uma operação [**\[ idempotente \]**](idempotent.md) .</span><span class="sxs-lookup"><span data-stu-id="7bfa6-123">An operation with the **\[broadcast\]** attribute is implicitly an [**\[idempotent\]**](idempotent.md) operation.</span></span> <span data-ttu-id="7bfa6-124">No entanto, o atributo **\[ Broadcast \]** Especifica propriedades adicionais que funções com o atributo **\[ idempotente \]** não têm.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-124">However, the **\[broadcast\]** attribute specifies additional properties that functions with the **\[idempotent\]** attribute don't have.</span></span> <span data-ttu-id="7bfa6-125">Especificamente, as funções que usam o atributo **\[ Broadcast \]** especificam que a rotina pode ser chamada várias vezes como o resultado de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-125">Specifically, functions using the **\[broadcast\]** attribute specify that the routine can be called multiple times as the result of one remote procedure call.</span></span> <span data-ttu-id="7bfa6-126">Ao mesmo tempo, eles podem ser enviados para vários servidores.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-126">At the same time, they can be sent to multiple servers.</span></span> <span data-ttu-id="7bfa6-127">Isso é diferente do atributo **\[ idempotente \]** , que especifica apenas que uma chamada pode ser repetida se não for concluída.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-127">This is different from the **\[idempotent\]** attribute, which specifies only that a call can be retried if it is not completed.</span></span>

<span data-ttu-id="7bfa6-128">Se um procedimento remoto transmite sua chamada para todos os hosts em uma rede local, ele deve usar a sequência de protocolo [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md) ou [**ncadg \_ IPX**](ncadg-ipx.md) .</span><span class="sxs-lookup"><span data-stu-id="7bfa6-128">If a remote procedure broadcasts its call to all hosts on a local network, it must use either the [**ncadg\_ip\_udp**](ncadg-ip-udp.md) or the [**ncadg\_ipx**](ncadg-ipx.md) protocol sequence.</span></span> <span data-ttu-id="7bfa6-129">Observe que o tamanho de um pacote de **\[ difusão \]** é determinado pelo serviço de datagrama em uso.</span><span class="sxs-lookup"><span data-stu-id="7bfa6-129">Note that the size of a **\[broadcast\]** packet is determined by the datagram service in use.</span></span>

## <a name="see-also"></a><span data-ttu-id="7bfa6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bfa6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bfa6-131">**idempotente**</span><span class="sxs-lookup"><span data-stu-id="7bfa6-131">**idempotent**</span></span>](idempotent.md)
</dt> <dt>

[<span data-ttu-id="7bfa6-132">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="7bfa6-132">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="7bfa6-133">**Eu**</span><span class="sxs-lookup"><span data-stu-id="7bfa6-133">**maybe**</span></span>](maybe.md)
</dt> <dt>

[<span data-ttu-id="7bfa6-134">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="7bfa6-134">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="7bfa6-135">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="7bfa6-135">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> </dl>

 

 




