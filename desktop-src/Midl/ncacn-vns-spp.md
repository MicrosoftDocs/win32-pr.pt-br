---
title: ncacn_vns_spp atributo
description: A \_ \_ palavra-chave ncacn VNS spp identifica Banyan Vines spp como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- ncacn_vns_spp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640794"
---
# <a name="ncacn_vns_spp-attribute"></a><span data-ttu-id="29e1d-105">\_atributo ncacn VNS \_ spp</span><span class="sxs-lookup"><span data-stu-id="29e1d-105">ncacn\_vns\_spp attribute</span></span>

<span data-ttu-id="29e1d-106">A palavra-chave **ncacn \_ VNS \_ spp** identifica Banyan Vines spp como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="29e1d-106">The **ncacn\_vns\_spp** keyword identifies Banyan Vines SPP as the protocol family for the endpoint.</span></span> <span data-ttu-id="29e1d-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="29e1d-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a><span data-ttu-id="29e1d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29e1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e1d-109">*nome do servidor*</span><span class="sxs-lookup"><span data-stu-id="29e1d-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="29e1d-110">Especifica o nome do StreetTalk do servidor.</span><span class="sxs-lookup"><span data-stu-id="29e1d-110">Specifies the StreetTalk name of the server.</span></span> <span data-ttu-id="29e1d-111">O nome está no formato item@group @organization .</span><span class="sxs-lookup"><span data-stu-id="29e1d-111">The name is of the form item@group@organization.</span></span> <span data-ttu-id="29e1d-112">O item pode ter até 31 caracteres de comprimento e o grupo e a organização podem ter até 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="29e1d-112">The item can be up to 31 characters long and the group and organization can be up to 15 characters.</span></span>

</dd> <dt>

<span data-ttu-id="29e1d-113">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="29e1d-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="29e1d-114">Especifica uma porta Banyan Vines SPP.</span><span class="sxs-lookup"><span data-stu-id="29e1d-114">Specifies a Banyan Vines SPP port.</span></span> <span data-ttu-id="29e1d-115">O intervalo válido para pontos de extremidade estáticos é 250 – 511.</span><span class="sxs-lookup"><span data-stu-id="29e1d-115">The valid range for static endpoints is 250– 511.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29e1d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="29e1d-116">Remarks</span></span>

<span data-ttu-id="29e1d-117">Para usar o protocolo de transporte **ncacn \_ VNS \_ spp** em aplicativos distribuídos em execução no Windows 2000, o software Banyan cliente corporativo apropriado deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="29e1d-117">In order to use the **ncacn\_vns\_spp** transport protocol in distributed applications running on Windows 2000, the appropriate Banyan Enterprise Client software must be installed.</span></span> <span data-ttu-id="29e1d-118">Após a instalação, abra o **painel de controle**, escolha **configuração e adicionar e**, em seguida, selecione **\| \| serviços de RPC de Banyan para Banyan**.</span><span class="sxs-lookup"><span data-stu-id="29e1d-118">After installation, open **Control Panel**, choose **Configuration and Add**, then select **Service \| Banyan \| RPC services for Banyan**.</span></span> <span data-ttu-id="29e1d-119">O suporte para clientes de 16 bits requer um software de Vines apropriado.</span><span class="sxs-lookup"><span data-stu-id="29e1d-119">Support for 16-bit clients requires appropriate Vines software.</span></span> <span data-ttu-id="29e1d-120">Para obter mais informações sobre o produto de Cliente Corporativo da Banyan e o software de Vines de 16 bits, entre em contato com a Banyan.</span><span class="sxs-lookup"><span data-stu-id="29e1d-120">For more information about Banyan's Enterprise Client product and 16-bit Vines software, contact Banyan.</span></span>

<span data-ttu-id="29e1d-121">A sintaxe da cadeia de caracteres de porta de transporte Banyan Vines SPP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="29e1d-121">The syntax of the Banyan Vines SPP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="29e1d-122">O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="29e1d-122">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="29e1d-123">Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="29e1d-123">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="29e1d-124">Não há suporte para essa família de protocolos no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29e1d-124">This protocol family is not supported in Windows XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="29e1d-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29e1d-125">Examples</span></span>

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="29e1d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="29e1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e1d-127">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="29e1d-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="29e1d-128">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="29e1d-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="29e1d-129">**ncacn \_ no \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="29e1d-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="29e1d-130">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="29e1d-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="29e1d-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="29e1d-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="29e1d-132">**IPX do ncacn \_ NB \_**</span><span class="sxs-lookup"><span data-stu-id="29e1d-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="29e1d-133">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="29e1d-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="29e1d-134">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="29e1d-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="29e1d-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="29e1d-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="29e1d-136">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="29e1d-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="29e1d-137">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="29e1d-137">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="29e1d-138">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="29e1d-138">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="29e1d-139">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="29e1d-139">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="29e1d-140">Associação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="29e1d-140">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 