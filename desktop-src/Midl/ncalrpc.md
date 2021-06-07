---
title: atributo Ncalrpc
description: A palavra-chave Ncalrpc identifica a comunicação entre processos local como a família de protocolos para o ponto de extremidade. Essa palavra-chave é um dos nomes de família de protocolos válidos que devem ser usados com o atributo \ Endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- Ncalrpc do atributo MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f5d22b572eb9ad2f2e46b029ec242b48d5cd684
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386875"
---
# <a name="ncalrpc-attribute"></a><span data-ttu-id="30344-105">atributo Ncalrpc</span><span class="sxs-lookup"><span data-stu-id="30344-105">ncalrpc attribute</span></span>

<span data-ttu-id="30344-106">A palavra-chave **Ncalrpc** identifica a comunicação entre processos local como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="30344-106">The **ncalrpc** keyword identifies local interprocess communication as the protocol family for the endpoint.</span></span> <span data-ttu-id="30344-107">Essa palavra-chave é um dos nomes de família de protocolos válidos que devem ser usados com o atributo de **\[** [**ponto de extremidade**](endpoint.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="30344-107">This keyword is one of the valid protocol family names that must be used with the **\[**[**endpoint**](endpoint.md)**\]** attribute.</span></span>

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="30344-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30344-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30344-109">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="30344-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="30344-110">Uma cadeia de caracteres que especifica a porta de comunicação (um aplicativo, um serviço ou uma instância de um serviço) que um cliente usa para fazer chamadas entre processos em um servidor.</span><span class="sxs-lookup"><span data-stu-id="30344-110">A character string that specifies the communication port (an application, a service, or an instance of a service) that a client uses to make interprocess calls to a server.</span></span> <span data-ttu-id="30344-111">A cadeia de caracteres pode conter até 53 caracteres e não deve conter nenhum caractere de barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="30344-111">The string can contain up to 53 characters and should not contain any backslash (\\) characters.</span></span> <span data-ttu-id="30344-112">O nome do computador não deve ser usado com a palavra-chave **Ncalrpc** .</span><span class="sxs-lookup"><span data-stu-id="30344-112">The computer name must not be used with the **ncalrpc** keyword.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30344-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="30344-113">Remarks</span></span>

<span data-ttu-id="30344-114">A sintaxe da cadeia de caracteres da porta de comunicação entre processos local, como todas as cadeias de porta, é definida pela implementação do transporte e é independente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="30344-114">The syntax of the local interprocess-communication port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="30344-115">O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="30344-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="30344-116">Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="30344-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="30344-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="30344-117">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="30344-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="30344-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30344-119">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="30344-119">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="30344-120">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="30344-120">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="30344-121">**ncacn \_ no \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="30344-121">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="30344-122">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="30344-122">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="30344-123">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="30344-123">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="30344-124">**IPX do ncacn \_ NB \_**</span><span class="sxs-lookup"><span data-stu-id="30344-124">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="30344-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="30344-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="30344-126">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="30344-126">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="30344-127">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="30344-127">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="30344-128">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="30344-128">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="30344-129">**ncacn \_ VNS \_ spp**</span><span class="sxs-lookup"><span data-stu-id="30344-129">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="30344-130">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="30344-130">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="30344-131">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="30344-131">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="30344-132">Associação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="30344-132">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 