---
title: ncacn_np atributo
description: A \_ palavra-chave ncacn NP identifica pipes nomeados como a família de protocolos para o ponto de extremidade.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np do atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640958"
---
# <a name="ncacn_np-attribute"></a><span data-ttu-id="307c9-104">\_atributo ncacn NP</span><span class="sxs-lookup"><span data-stu-id="307c9-104">ncacn\_np attribute</span></span>

<span data-ttu-id="307c9-105">A palavra-chave **ncacn \_ NP** identifica pipes nomeados como a família de protocolos para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="307c9-105">The **ncacn\_np** keyword identifies named pipes as the protocol family for the endpoint.</span></span>

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a><span data-ttu-id="307c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="307c9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="307c9-107">*nome do servidor*</span><span class="sxs-lookup"><span data-stu-id="307c9-107">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="307c9-108">Opcional.</span><span class="sxs-lookup"><span data-stu-id="307c9-108">Optional.</span></span> <span data-ttu-id="307c9-109">Especifica o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="307c9-109">Specifies the name of the server.</span></span> <span data-ttu-id="307c9-110">Caracteres de barra invertida são opcionais.</span><span class="sxs-lookup"><span data-stu-id="307c9-110">Backslash characters are optional.</span></span>

</dd> <dt>

<span data-ttu-id="307c9-111">*nome do pipe*</span><span class="sxs-lookup"><span data-stu-id="307c9-111">*pipe-name*</span></span> 
</dt> <dd>

<span data-ttu-id="307c9-112">Especifica um nome de pipe válido.</span><span class="sxs-lookup"><span data-stu-id="307c9-112">Specifies a valid pipe name.</span></span> <span data-ttu-id="307c9-113">Um nome de pipe válido é uma cadeia de caracteres que contém identificadores separados por caracteres de barra invertida.</span><span class="sxs-lookup"><span data-stu-id="307c9-113">A valid pipe name is a string containing identifiers separated by backslash characters.</span></span> <span data-ttu-id="307c9-114">O primeiro identificador deve ser [**pipe**](pipe.md).</span><span class="sxs-lookup"><span data-stu-id="307c9-114">The first identifier must be [**pipe**](pipe.md).</span></span> <span data-ttu-id="307c9-115">Cada identificador deve ser separado por dois caracteres de barra invertida.</span><span class="sxs-lookup"><span data-stu-id="307c9-115">Each identifier must be separated by two backslash characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="307c9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="307c9-116">Remarks</span></span>

<span data-ttu-id="307c9-117">Um servidor cria uma instância de um pipe nomeado que está disponível para qualquer cliente.</span><span class="sxs-lookup"><span data-stu-id="307c9-117">A server creates an instance of a named pipe that is then available to any client.</span></span> <span data-ttu-id="307c9-118">Quando um cliente tenta se conectar, a instância existente é associada a esse cliente.</span><span class="sxs-lookup"><span data-stu-id="307c9-118">When a client attempts to connect, the existing instance is associated with that client.</span></span> <span data-ttu-id="307c9-119">Antes que outro cliente possa se conectar, o servidor deve criar outra instância do pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="307c9-119">Before another client can connect, the server must create another instance of the named pipe.</span></span> <span data-ttu-id="307c9-120">Se um cliente tentar se associar ao servidor antes que a nova instância seja criada, a chamada de associação, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), poderá falhar com a mensagem de erro o servidor RPC está \_ \_ \_ muito \_ ocupado.</span><span class="sxs-lookup"><span data-stu-id="307c9-120">If a client tries to bind to the server before the new instance is created, the binding call, [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), may fail with the error message RPC\_S\_SERVER\_TOO\_BUSY.</span></span> <span data-ttu-id="307c9-121">Portanto, você precisa garantir que o aplicativo cliente manipule o caso em que o servidor está muito ocupado para aceitar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="307c9-121">Therefore, you need to make sure that your client application handles the case where the server is too busy to accept a connection.</span></span> <span data-ttu-id="307c9-122">O cliente deve repetir automaticamente, solicitar um curso de ação ao usuário ou falhar normalmente.</span><span class="sxs-lookup"><span data-stu-id="307c9-122">The client should automatically retry, prompt the user for a course of action, or fail gracefully.</span></span>

<span data-ttu-id="307c9-123">A sintaxe da cadeia de caracteres de porta de pipe nomeado, como todas as cadeias de caracteres de porta, é definida pela implementação de transporte e é independente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="307c9-123">The syntax of the named-pipe port string, like all port strings, is defined by the transport implementation and is independent of the IDL specification.</span></span> <span data-ttu-id="307c9-124">O compilador MIDL executa uma verificação de sintaxe limitada, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="307c9-124">The MIDL compiler performs limited syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="307c9-125">Algumas classes de erros podem ser relatadas em tempo de execução em vez de em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="307c9-125">Some classes of errors may be reported at run time rather than at compile time.</span></span>

## <a name="examples"></a><span data-ttu-id="307c9-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="307c9-126">Examples</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
] 
interface iface2
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="307c9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="307c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307c9-128">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="307c9-128">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="307c9-129">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="307c9-129">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="307c9-130">**ncacn \_ no \_ DSP**</span><span class="sxs-lookup"><span data-stu-id="307c9-130">**ncacn\_at\_dsp**</span></span>](ncacn-at-dsp.md)
</dt> <dt>

[<span data-ttu-id="307c9-131">**ncacn \_ dnet \_ NSP**</span><span class="sxs-lookup"><span data-stu-id="307c9-131">**ncacn\_dnet\_nsp**</span></span>](ncacn-dnet-nsp.md)
</dt> <dt>

[<span data-ttu-id="307c9-132">**\_TCP IP \_ ncacn**</span><span class="sxs-lookup"><span data-stu-id="307c9-132">**ncacn\_ip\_tcp**</span></span>](ncacn-ip-tcp.md)
</dt> <dt>

[<span data-ttu-id="307c9-133">**IPX do ncacn \_ NB \_**</span><span class="sxs-lookup"><span data-stu-id="307c9-133">**ncacn\_nb\_ipx**</span></span>](ncacn-nb-ipx.md)
</dt> <dt>

[<span data-ttu-id="307c9-134">**ncacn \_ SPX**</span><span class="sxs-lookup"><span data-stu-id="307c9-134">**ncacn\_spx**</span></span>](ncacn-spx.md)
</dt> <dt>

[<span data-ttu-id="307c9-135">**ncacn \_ NB NB \_**</span><span class="sxs-lookup"><span data-stu-id="307c9-135">**ncacn\_nb\_nb**</span></span>](ncacn-nb-nb.md)
</dt> <dt>

[<span data-ttu-id="307c9-136">**ncacn \_ NB \_ TCP**</span><span class="sxs-lookup"><span data-stu-id="307c9-136">**ncacn\_nb\_tcp**</span></span>](ncacn-nb-tcp.md)
</dt> <dt>

[<span data-ttu-id="307c9-137">**ncacn \_ VNS \_ spp**</span><span class="sxs-lookup"><span data-stu-id="307c9-137">**ncacn\_vns\_spp**</span></span>](ncacn-vns-spp.md)
</dt> <dt>

[<span data-ttu-id="307c9-138">**ncalrpc**</span><span class="sxs-lookup"><span data-stu-id="307c9-138">**ncalrpc**</span></span>](ncalrpc.md)
</dt> <dt>

[<span data-ttu-id="307c9-139">**ncadg \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="307c9-139">**ncadg\_ipx**</span></span>](ncadg-ipx.md)
</dt> <dt>

[<span data-ttu-id="307c9-140">**\_UDP IP \_ ncadg**</span><span class="sxs-lookup"><span data-stu-id="307c9-140">**ncadg\_ip\_udp**</span></span>](ncadg-ip-udp.md)
</dt> <dt>

[<span data-ttu-id="307c9-141">**Associação de cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="307c9-141">**string binding**</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 