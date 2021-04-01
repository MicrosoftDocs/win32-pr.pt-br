---
title: ncadg_ip_udp atributo
description: A \_ \_ palavra-chave UDP IP ncadg identifica a versão do datagrama do TCP/IP como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp do atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084488"
---
# <a name="ncadg_ip_udp-attribute"></a><span data-ttu-id="a1b12-105">\_atributo UDP de IP ncadg \_</span><span class="sxs-lookup"><span data-stu-id="a1b12-105">ncadg\_ip\_udp attribute</span></span>

<span data-ttu-id="a1b12-106">A palavra-chave **\_ \_ UDP IP ncadg** identifica a versão do datagrama do TCP/IP como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a1b12-106">The **ncadg\_ip\_udp** keyword identifies the datagram version of TCP/IP as the protocol family for the endpoint.</span></span> <span data-ttu-id="a1b12-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a1b12-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="a1b12-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1b12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1b12-109">*nome do servidor*</span><span class="sxs-lookup"><span data-stu-id="a1b12-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b12-110">Especifica o nome ou endereço de Internet para o servidor, ou host, computador.</span><span class="sxs-lookup"><span data-stu-id="a1b12-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="a1b12-111">O nome é uma cadeia de caracteres e pode ser um nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="a1b12-111">The name is a character string and may be a fully qualified domain name.</span></span> <span data-ttu-id="a1b12-112">O endereço da Internet é uma notação de endereço da Internet comum.</span><span class="sxs-lookup"><span data-stu-id="a1b12-112">The internet address is a common internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="a1b12-113">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="a1b12-113">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a1b12-114">Especifica um número opcional de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b12-114">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="a1b12-115">Valores menores que 1024 geralmente são reservados.</span><span class="sxs-lookup"><span data-stu-id="a1b12-115">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="a1b12-116">Se nenhum valor for especificado, o serviço de mapeamento de ponto de extremidade selecionará um valor *de nome de porta* válido.</span><span class="sxs-lookup"><span data-stu-id="a1b12-116">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1b12-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1b12-117">Remarks</span></span>

<span data-ttu-id="a1b12-118">As restrições a seguir se aplicam aos protocolos de datagrama, [**ncadg \_ IPX**](ncadg-ipx.md) e **ncadg \_ IP \_ UDP**:</span><span class="sxs-lookup"><span data-stu-id="a1b12-118">The following restrictions apply to the datagram protocols, [**ncadg\_ipx**](ncadg-ipx.md) and **ncadg\_ip\_udp**:</span></span>

-   <span data-ttu-id="a1b12-119">Eles não oferecem suporte a retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="a1b12-119">They do not support callbacks.</span></span> <span data-ttu-id="a1b12-120">Qualquer função que use o atributo de **\[** [**retorno de chamada**](callback.md) **\]** falhará.</span><span class="sxs-lookup"><span data-stu-id="a1b12-120">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="a1b12-121">Eles não dão suporte ao uso do construtor de tipo de [**pipe**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b12-121">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="a1b12-122">A sintaxe da cadeia de caracteres da porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL.</span><span class="sxs-lookup"><span data-stu-id="a1b12-122">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="a1b12-123">O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="a1b12-123">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="a1b12-124">Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="a1b12-124">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="a1b12-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1b12-125">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="a1b12-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1b12-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1b12-127">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="a1b12-127">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="a1b12-128">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="a1b12-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a1b12-129">**ncacn \_ no \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="a1b12-129">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="a1b12-130">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="a1b12-130">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="a1b12-131">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="a1b12-131">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="a1b12-132">**IPX do ncacn \_ NB \_**</span><span class="sxs-lookup"><span data-stu-id="a1b12-132">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="a1b12-133">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="a1b12-133">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="a1b12-134">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="a1b12-134">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="a1b12-135">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="a1b12-135">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="a1b12-136">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="a1b12-136">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="a1b12-137">**ncacn \_ VNS \_ spp**</span><span class="sxs-lookup"><span data-stu-id="a1b12-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="a1b12-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="a1b12-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="a1b12-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="a1b12-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="a1b12-140">Associação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a1b12-140">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 