---
title: ncacn_nb_tcp atributo
description: A \_ \_ palavra-chave TCP do NB ncacn é usada para identificar o TCP sobre NetBIOS como a família de protocolos para o ponto de extremidade. Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- ncacn_nb_tcp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294014"
---
# <a name="ncacn_nb_tcp-attribute"></a><span data-ttu-id="c7695-105">\_atributo TCP de NB ncacn \_</span><span class="sxs-lookup"><span data-stu-id="c7695-105">ncacn\_nb\_tcp attribute</span></span>

<span data-ttu-id="c7695-106">A palavra-chave **\_ \_ TCP do NB ncacn** é usada para identificar o TCP sobre NetBIOS como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c7695-106">The **ncacn\_nb\_tcp** keyword is used to identify TCP over NetBIOS as the protocol family for the endpoint.</span></span> <span data-ttu-id="c7695-107">Esta família de protocolos está obsoleta e não deve ser usada em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c7695-107">This protocol family is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="c7695-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7695-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7695-109">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="c7695-109">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c7695-110">Especifica um valor opcional de 8 bits que varia de 1 a 254.</span><span class="sxs-lookup"><span data-stu-id="c7695-110">Specifies an optional 8-bit value ranging from 1 to 254.</span></span> <span data-ttu-id="c7695-111">Valores menores que 0x20 são reservados.</span><span class="sxs-lookup"><span data-stu-id="c7695-111">Values of less than 0x20 are reserved.</span></span> <span data-ttu-id="c7695-112">Se o valor de *Port-Name* não for especificado, o serviço de mapeamento de ponto de extremidade selecionará o valor da porta.</span><span class="sxs-lookup"><span data-stu-id="c7695-112">If the *port-name* value is not specified, the endpoint-mapping service selects the port value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7695-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7695-113">Remarks</span></span>

<span data-ttu-id="c7695-114">A sintaxe da cadeia de caracteres de porta NetBIOS, como todas as cadeias de porta, é definida pela implementação de transporte e é independente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="c7695-114">The syntax of the NetBIOS port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="c7695-115">O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="c7695-115">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="c7695-116">Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="c7695-116">Some classes of errors may be reported at run time rather than at compile time.</span></span>

> [!Note]  
> <span data-ttu-id="c7695-117">Não há suporte para essa família de protocolos no WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="c7695-117">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c7695-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c7695-118">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_tcp:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c7695-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7695-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7695-120">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="c7695-120">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c7695-121">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="c7695-121">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c7695-122">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="c7695-122">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="c7695-123">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="c7695-123">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="c7695-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="c7695-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="c7695-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="c7695-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="c7695-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="c7695-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="c7695-127">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c7695-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 