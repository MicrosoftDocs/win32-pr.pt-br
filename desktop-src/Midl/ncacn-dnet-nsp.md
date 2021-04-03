---
title: ncacn_dnet_nsp atributo
description: A \_ \_ palavra-chave ncacn dnet NSP identifica o DECnet como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084525"
---
# <a name="ncacn_dnet_nsp-attribute"></a><span data-ttu-id="a8c33-105">\_atributo ncacn dnet \_ NSP</span><span class="sxs-lookup"><span data-stu-id="a8c33-105">ncacn\_dnet\_nsp attribute</span></span>

<span data-ttu-id="a8c33-106">A palavra-chave **ncacn \_ dnet \_ NSP** identifica o DECnet como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a8c33-106">The **ncacn\_dnet\_nsp** keyword identifies DECnet as the protocol family for the endpoint.</span></span> <span data-ttu-id="a8c33-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="a8c33-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="a8c33-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8c33-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8c33-109">*nome do servidor*</span><span class="sxs-lookup"><span data-stu-id="a8c33-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a8c33-110">Especifica o nome ou endereço de Internet para o servidor, ou host, computador.</span><span class="sxs-lookup"><span data-stu-id="a8c33-110">Specifies the name or internet address for the server, or host, computer.</span></span> <span data-ttu-id="a8c33-111">O nome é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8c33-111">The name is a character string.</span></span>

</dd> <dt>

<span data-ttu-id="a8c33-112">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="a8c33-112">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="a8c33-113">Especifica um nome de objeto ou número de objeto DECnet.</span><span class="sxs-lookup"><span data-stu-id="a8c33-113">Specifies a DECnet object name or object number.</span></span> <span data-ttu-id="a8c33-114">O nome do objeto pode consistir em até 16 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8c33-114">The object name can consist of up to 16 characters.</span></span> <span data-ttu-id="a8c33-115">Os números de objeto podem ser prefixados pelo sinal de libra ( \# ).</span><span class="sxs-lookup"><span data-stu-id="a8c33-115">Object numbers can be prefixed by the pound sign (\#).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8c33-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8c33-116">Remarks</span></span>

<span data-ttu-id="a8c33-117">A sintaxe da cadeia de caracteres da porta de transporte DECnet, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL.</span><span class="sxs-lookup"><span data-stu-id="a8c33-117">The syntax of the DECnet transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="a8c33-118">O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="a8c33-118">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="a8c33-119">Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="a8c33-119">Some errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="a8c33-120">Não há suporte para essa família de protocolos no WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="a8c33-120">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a8c33-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a8c33-121">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="a8c33-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8c33-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8c33-123">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="a8c33-123">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="a8c33-124">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8c33-124">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 