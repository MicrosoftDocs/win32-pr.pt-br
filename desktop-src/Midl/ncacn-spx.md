---
title: ncacn_spx atributo
description: A \_ palavra-chave ncacn SPX identifica SPX como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105764674"
---
# <a name="ncacn_spx-attribute"></a><span data-ttu-id="8c60b-105">\_atributo ncacn SPX</span><span class="sxs-lookup"><span data-stu-id="8c60b-105">ncacn\_spx attribute</span></span>

<span data-ttu-id="8c60b-106">A palavra-chave **ncacn \_ SPX** identifica SPX como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="8c60b-106">The **ncacn\_spx** keyword identifies SPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="8c60b-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8c60b-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="8c60b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c60b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c60b-109">*Endereço de link*</span><span class="sxs-lookup"><span data-stu-id="8c60b-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="8c60b-110">Especifica o servidor host.</span><span class="sxs-lookup"><span data-stu-id="8c60b-110">Specifies the host server.</span></span> <span data-ttu-id="8c60b-111">Pode ser uma cadeia de caracteres (o nome do servidor) ou um número hexadecimal de 20 dígitos que consiste no endereço de rede do servidor host (8 dígitos) concatenado com o endereço do nó (12 dígitos).</span><span class="sxs-lookup"><span data-stu-id="8c60b-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="8c60b-112">Consulte comentários para obter instruções sobre como obter o endereço de rede e o endereço do nó.</span><span class="sxs-lookup"><span data-stu-id="8c60b-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="8c60b-113">Uma cadeia de caracteres **nula** especifica o computador local.</span><span class="sxs-lookup"><span data-stu-id="8c60b-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8c60b-114">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="8c60b-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="8c60b-115">Especifica um número opcional de 16 bits que representa o endereço do soquete.</span><span class="sxs-lookup"><span data-stu-id="8c60b-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="8c60b-116">Os valores podem variar de 1 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="8c60b-116">Values can range from 1 to 65,535.</span></span> <span data-ttu-id="8c60b-117">Quando nenhum valor é especificado, o serviço de mapeamento de ponto de extremidade seleciona um valor *de nome de porta* válido.</span><span class="sxs-lookup"><span data-stu-id="8c60b-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c60b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c60b-118">Remarks</span></span>

<span data-ttu-id="8c60b-119">Quando você usa o transporte **ncacn \_ SPX** , o nome do servidor é exatamente o mesmo que o nome do Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8c60b-119">When you use the **ncacn\_spx** transport, the server name is exactly the same as the 32-bit Windows name.</span></span> <span data-ttu-id="8c60b-120">No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenclatura da Novell.</span><span class="sxs-lookup"><span data-stu-id="8c60b-120">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="8c60b-121">Se um nome de servidor não for um nome Novell válido, os servidores não poderão criar pontos de extremidade com o transporte **ncacn \_ SPX** .</span><span class="sxs-lookup"><span data-stu-id="8c60b-121">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncacn\_spx** transport.</span></span> <span data-ttu-id="8c60b-122">A seguir está uma lista parcial de caracteres proibidos em nomes de servidor Novell:</span><span class="sxs-lookup"><span data-stu-id="8c60b-122">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="8c60b-123">" \* + .</span><span class="sxs-lookup"><span data-stu-id="8c60b-123">" \* + .</span></span> <span data-ttu-id="8c60b-124">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="8c60b-124">/ : ; < = > ?</span></span> <span data-ttu-id="8c60b-125">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="8c60b-125">\[ \] \\ \|</span></span>

<span data-ttu-id="8c60b-126">O transporte **ncacn \_ SPX** não é compatível com a versão do NWLink fornecida com o MS Client 3,0.</span><span class="sxs-lookup"><span data-stu-id="8c60b-126">The **ncacn\_spx** transport is not supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="8c60b-127">aplicativos cliente do Windows de 16 bits que usam o transporte **ncacn \_ SPX** exigem que o arquivo Nwipxspx.dll ser instalado para ser executado no subsistema WOW.</span><span class="sxs-lookup"><span data-stu-id="8c60b-127">16-bit Windows client applications that use the **ncacn\_spx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="8c60b-128">Contate a Novell para obter esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c60b-128">Contact Novell to obtain this file.</span></span>

> [!Note]  
> <span data-ttu-id="8c60b-129">Para obter os endereços de rede e nó, use o utilitário **ComCheck** do Novell ou a API definida pela Novell **IPXGetInternetAddress**.</span><span class="sxs-lookup"><span data-stu-id="8c60b-129">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="8c60b-130">No Windows, você também pode obter esses endereços com o comando **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="8c60b-130">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

 

<span data-ttu-id="8c60b-131">A sintaxe da cadeia de caracteres da porta de transporte SPX, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL.</span><span class="sxs-lookup"><span data-stu-id="8c60b-131">The syntax of the SPX transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="8c60b-132">O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="8c60b-132">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="8c60b-133">Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="8c60b-133">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="8c60b-134">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c60b-134">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="8c60b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c60b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c60b-136">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="8c60b-136">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="8c60b-137">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="8c60b-137">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="8c60b-138">**ncacn \_ no \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="8c60b-138">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="8c60b-139">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="8c60b-139">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="8c60b-140">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="8c60b-140">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="8c60b-141">**IPX do ncacn \_ NB \_**</span><span class="sxs-lookup"><span data-stu-id="8c60b-141">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="8c60b-142">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="8c60b-142">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="8c60b-143">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="8c60b-143">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="8c60b-144">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="8c60b-144">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="8c60b-145">**ncacn \_ VNS \_ spp**</span><span class="sxs-lookup"><span data-stu-id="8c60b-145">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="8c60b-146">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="8c60b-146">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="8c60b-147">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="8c60b-147">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="8c60b-148">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="8c60b-148">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="8c60b-149">Associação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="8c60b-149">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 