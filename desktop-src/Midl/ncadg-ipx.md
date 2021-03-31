---
title: ncadg_ipx atributo
description: A \_ palavra-chave IPX ncadg identifica o IPX como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx do atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa206902ae80e5218e1d5249da8a8fb1b9dfc04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640619"
---
# <a name="ncadg_ipx-attribute"></a><span data-ttu-id="77d50-105">\_atributo IPX ncadg</span><span class="sxs-lookup"><span data-stu-id="77d50-105">ncadg\_ipx attribute</span></span>

<span data-ttu-id="77d50-106">A palavra-chave **\_ IPX ncadg** identifica o IPX como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="77d50-106">The **ncadg\_ipx** keyword identifies IPX as the protocol family for the endpoint.</span></span> <span data-ttu-id="77d50-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="77d50-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="77d50-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77d50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77d50-109">*Endereço de link*</span><span class="sxs-lookup"><span data-stu-id="77d50-109">*link-address*</span></span> 
</dt> <dd>

<span data-ttu-id="77d50-110">Especifica o servidor host.</span><span class="sxs-lookup"><span data-stu-id="77d50-110">Specifies the host server.</span></span> <span data-ttu-id="77d50-111">Pode ser uma cadeia de caracteres (o nome do servidor) ou um número hexadecimal de 20 dígitos que consiste no endereço de rede do servidor host (8 dígitos) concatenado com o endereço do nó (12 dígitos).</span><span class="sxs-lookup"><span data-stu-id="77d50-111">This may be either a character string (the server name), or a 20-digit hexadecimal number that consists of the host server's network address (8 digits) concatenated with the node address (12 digits).</span></span> <span data-ttu-id="77d50-112">Consulte comentários para obter instruções sobre como obter o endereço de rede e o endereço do nó.</span><span class="sxs-lookup"><span data-stu-id="77d50-112">See Remarks for instructions on how to obtain the network address and node address.</span></span> <span data-ttu-id="77d50-113">Uma cadeia de caracteres **nula** especifica o computador local.</span><span class="sxs-lookup"><span data-stu-id="77d50-113">A **NULL** string specifies the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="77d50-114">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="77d50-114">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="77d50-115">Especifica um número opcional de 16 bits que representa o endereço do soquete.</span><span class="sxs-lookup"><span data-stu-id="77d50-115">Specifies an optional 16-bit number that represents the socket address.</span></span> <span data-ttu-id="77d50-116">Os valores podem variar de 1 a 65535.</span><span class="sxs-lookup"><span data-stu-id="77d50-116">Values can range from 1 to 65535.</span></span> <span data-ttu-id="77d50-117">Quando nenhum valor é especificado, o serviço de mapeamento de ponto de extremidade seleciona um valor *de nome de porta* válido.</span><span class="sxs-lookup"><span data-stu-id="77d50-117">When no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77d50-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="77d50-118">Remarks</span></span>

<span data-ttu-id="77d50-119">As restrições a seguir se aplicam aos protocolos de datagrama, **ncadg \_ IPX** e [**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md):</span><span class="sxs-lookup"><span data-stu-id="77d50-119">The following restrictions apply to the datagram protocols, **ncadg\_ipx** and [**ncadg\_ip\_udp**](ncadg-ip-udp.md):</span></span>

-   <span data-ttu-id="77d50-120">Eles não oferecem suporte a retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="77d50-120">They do not support callbacks.</span></span> <span data-ttu-id="77d50-121">Qualquer função que use o atributo de **\[** [**retorno de chamada**](callback.md) **\]** falhará.</span><span class="sxs-lookup"><span data-stu-id="77d50-121">Any functions using the **\[**[**callback**](callback.md)**\]** attribute will fail.</span></span>
-   <span data-ttu-id="77d50-122">Eles não dão suporte ao uso do construtor de tipo de [**pipe**](pipe.md) .</span><span class="sxs-lookup"><span data-stu-id="77d50-122">They do not support use of the [**pipe**](pipe.md) type constructor.</span></span>

<span data-ttu-id="77d50-123">Ao usar o **transporte \_ IPX ncadg** , o nome do servidor é exatamente o mesmo que o nome do Windows Server de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="77d50-123">When using the **ncadg\_ipx** transport, the server name is exactly the same as the 32-bit Windows server name.</span></span> <span data-ttu-id="77d50-124">No entanto, como os nomes são distribuídos usando protocolos Novell, eles devem estar em conformidade com as convenções de nomenclatura da Novell.</span><span class="sxs-lookup"><span data-stu-id="77d50-124">However, since the names are distributed using Novell protocols, they must conform to the Novell naming conventions.</span></span> <span data-ttu-id="77d50-125">Se um nome de servidor não for um nome Novell válido, os servidores não poderão criar pontos de extremidade com o transporte **\_ IPX ncadg** .</span><span class="sxs-lookup"><span data-stu-id="77d50-125">If a server name is not a valid Novell name, servers will not be able to create endpoints with the **ncadg\_ipx** transport.</span></span> <span data-ttu-id="77d50-126">A seguir está uma lista parcial de caracteres proibidos em nomes de servidor Novell:</span><span class="sxs-lookup"><span data-stu-id="77d50-126">The following is a partial list of characters prohibited in Novell server names:</span></span>

<span data-ttu-id="77d50-127">" \* + .</span><span class="sxs-lookup"><span data-stu-id="77d50-127">" \* + .</span></span> <span data-ttu-id="77d50-128">/ : ; < = >?</span><span class="sxs-lookup"><span data-stu-id="77d50-128">/ : ; < = > ?</span></span> <span data-ttu-id="77d50-129">\[ \] \\ \|</span><span class="sxs-lookup"><span data-stu-id="77d50-129">\[ \] \\ \|</span></span>

<span data-ttu-id="77d50-130">O **transporte \_ IPX ncadg** é compatível com a versão do NWLink fornecida com o MS Client 3,0.</span><span class="sxs-lookup"><span data-stu-id="77d50-130">The **ncadg\_ipx** transport is supported by the version of NWLink supplied with MS Client 3.0.</span></span>

<span data-ttu-id="77d50-131">aplicativos cliente do Windows de 16 bits que usam o transporte **\_ IPX ncadg** exigem que o arquivo Nwipxspx.dll ser instalado para ser executado no subsistema WOW.</span><span class="sxs-lookup"><span data-stu-id="77d50-131">16-bit Windows client applications that use the **ncadg\_ipx** transport require that the file Nwipxspx.dll be installed in order to run under the WOW subsystem.</span></span> <span data-ttu-id="77d50-132">Contate a Novell para obter esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="77d50-132">Contact Novell to obtain this file.</span></span>

<span data-ttu-id="77d50-133">Para obter os endereços de rede e nó, use o utilitário **ComCheck** do Novell ou a API definida pela Novell **IPXGetInternetAddress**.</span><span class="sxs-lookup"><span data-stu-id="77d50-133">To obtain the network and node addresses, use Novell's **comcheck** utility, or the Novell-defined API **IPXGetInternetAddress**.</span></span> <span data-ttu-id="77d50-134">No Windows, você também pode obter esses endereços com o comando **ipxroute config** .</span><span class="sxs-lookup"><span data-stu-id="77d50-134">On Windows, you can also obtain these addresses with the **ipxroute config** command.</span></span>

<span data-ttu-id="77d50-135">A sintaxe da cadeia de caracteres da porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL.</span><span class="sxs-lookup"><span data-stu-id="77d50-135">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="77d50-136">O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="77d50-136">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="77d50-137">Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="77d50-137">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="77d50-138">Não há suporte para essa família de protocolos no WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="77d50-138">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="77d50-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="77d50-139">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="77d50-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="77d50-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77d50-141">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="77d50-141">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="77d50-142">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="77d50-142">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="77d50-143">**ncacn \_ no \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="77d50-143">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="77d50-144">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="77d50-144">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="77d50-145">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="77d50-145">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="77d50-146">**IPX do ncacn \_ NB \_**</span><span class="sxs-lookup"><span data-stu-id="77d50-146">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="77d50-147">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="77d50-147">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="77d50-148">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="77d50-148">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="77d50-149">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="77d50-149">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="77d50-150">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="77d50-150">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="77d50-151">**ncacn \_ VNS \_ spp**</span><span class="sxs-lookup"><span data-stu-id="77d50-151">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="77d50-152">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="77d50-152">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="77d50-153">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="77d50-153">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="77d50-154">Associação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="77d50-154">string binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 