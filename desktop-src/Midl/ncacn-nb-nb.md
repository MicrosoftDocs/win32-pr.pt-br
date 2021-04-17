---
title: ncacn_nb_nb atributo
description: A \_ \_ palavra-chave NB do ncacn NB identifica NetBEUI sobre NetBIOS como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105754658"
---
# <a name="ncacn_nb_nb-attribute"></a><span data-ttu-id="fa6dd-105">\_ \_ atributo NB do ncacn NB</span><span class="sxs-lookup"><span data-stu-id="fa6dd-105">ncacn\_nb\_nb attribute</span></span>

<span data-ttu-id="fa6dd-106">A palavra-chave **\_ \_ NB do ncacn NB** identifica NetBEUI sobre NetBIOS como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-106">The **ncacn\_nb\_nb** keyword identifies NetBEUI over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="fa6dd-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="fa6dd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa6dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa6dd-109">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="fa6dd-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fa6dd-110">Especifica um valor opcional de 8 bits que varia de 1 a 255.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-110">Specifies an optional 8-bit value ranging from 1 to 255.</span></span> <span data-ttu-id="fa6dd-111">Valores menores que 0x20 são reservados.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="fa6dd-112">Se o valor de *Port-Name* não for especificado, o serviço de mapeamento de ponto de extremidade selecionará o valor da porta.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa6dd-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa6dd-113">Remarks</span></span>

<span data-ttu-id="fa6dd-114">A sintaxe da cadeia de caracteres de porta NetBIOS, como todas as cadeias de porta, é definida pela implementação de transporte e é independente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="fa6dd-115">O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="fa6dd-116">Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="fa6dd-117">Não há suporte para essa família de protocolos no WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="fa6dd-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="fa6dd-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fa6dd-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="fa6dd-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa6dd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6dd-120">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-121">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="fa6dd-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="fa6dd-127">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="fa6dd-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 