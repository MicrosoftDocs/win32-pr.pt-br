---
title: ncacn_ip_tcp atributo
description: A \_ \_ palavra-chave TCP IP NCACN identifica TCP/IP como a família de protocolos para o ponto de extremidade.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105748170"
---
# <a name="ncacn_ip_tcp-attribute"></a><span data-ttu-id="880be-104">\_atributo TCP de IP ncacn \_</span><span class="sxs-lookup"><span data-stu-id="880be-104">ncacn\_ip\_tcp attribute</span></span>

<span data-ttu-id="880be-105">A palavra-chave **\_ \_ TCP IP ncacn** identifica TCP/IP como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="880be-105">The **ncacn\_ip\_tcp** keyword identifies TCP/IP as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a><span data-ttu-id="880be-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="880be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="880be-107">*nome do servidor*</span><span class="sxs-lookup"><span data-stu-id="880be-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="880be-108">Especifica o nome ou endereço de Internet para o servidor, ou host, computador.</span><span class="sxs-lookup"><span data-stu-id="880be-108">Specifies the name or Internet address for the server, or host, computer.</span></span> <span data-ttu-id="880be-109">O nome é uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="880be-109">The name is a character string.</span></span> <span data-ttu-id="880be-110">O endereço da Internet é uma notação de endereço da Internet comum.</span><span class="sxs-lookup"><span data-stu-id="880be-110">The Internet address is a common Internet address notation.</span></span>

</dd> <dt>

<span data-ttu-id="880be-111">*nome da porta*</span><span class="sxs-lookup"><span data-stu-id="880be-111">*port-name*</span></span> 
</dt> <dd>

<span data-ttu-id="880be-112">Especifica um número opcional de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="880be-112">Specifies an optional 16-bit number.</span></span> <span data-ttu-id="880be-113">Valores menores que 1024 geralmente são reservados.</span><span class="sxs-lookup"><span data-stu-id="880be-113">Values of less than 1024 are usually reserved.</span></span> <span data-ttu-id="880be-114">Se nenhum valor for especificado, o serviço de mapeamento de ponto de extremidade selecionará um valor *de nome de porta* válido.</span><span class="sxs-lookup"><span data-stu-id="880be-114">If no value is specified, the endpoint-mapping service selects a valid *port-name* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="880be-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="880be-115">Remarks</span></span>

<span data-ttu-id="880be-116">A sintaxe da cadeia de caracteres da porta de transporte TCP/IP, como todas as cadeias de caracteres de porta, é definida independentemente da especificação IDL.</span><span class="sxs-lookup"><span data-stu-id="880be-116">The syntax of the TCP/IP transport port string, like all port strings, is defined independently of the IDL specification.</span></span> <span data-ttu-id="880be-117">O compilador executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="880be-117">The compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="880be-118">Alguns erros podem ser relatados em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="880be-118">Some errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="880be-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="880be-119">Examples</span></span>

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a><span data-ttu-id="880be-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="880be-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="880be-121">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="880be-121">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="880be-122">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="880be-122">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="880be-123">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="880be-123">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="880be-124">**ncacn \_ NP**</span><span class="sxs-lookup"><span data-stu-id="880be-124">**ncacn\_np**</span></span>](ncacn-np.md)
</dt> <dt>

[<span data-ttu-id="880be-125">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="880be-125">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="880be-126">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="880be-126">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="880be-127">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="880be-127">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 