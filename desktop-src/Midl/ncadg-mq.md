---
title: ncadg_mq atributo
description: A \_ palavra-chave ncadg MQ identifica os serviços de enfileiramento de mensagens da Microsoft (MSMQ) como o protocolo de transporte para o ponto de extremidade. Esse protocolo está obsoleto e não deve ser usado em novos aplicativos.
ms.assetid: 7472fc47-c1f0-4578-8aef-b655505e0563
keywords:
- ncadg_mq do atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_mq
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0acc433b55ba9f3c6d8919bef9b8db470bc0f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917220"
---
# <a name="ncadg_mq-attribute"></a><span data-ttu-id="c0d27-105">\_atributo ncadg MQ</span><span class="sxs-lookup"><span data-stu-id="c0d27-105">ncadg\_mq attribute</span></span>

<span data-ttu-id="c0d27-106">A palavra-chave **ncadg \_ MQ** identifica os serviços de enfileiramento de mensagens da Microsoft (MSMQ) como o protocolo de transporte para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="c0d27-106">The **ncadg\_mq** keyword identifies Microsoft Message Queuing Services (MSMQ) as the transport protocol for the endpoint.</span></span> <span data-ttu-id="c0d27-107">Esse protocolo está obsoleto e não deve ser usado em novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c0d27-107">This protocol is obsolete and should not be used in new applications.</span></span>

``` syntax
endpoint("ncadg_mq:server-name")
```

## <a name="parameters"></a><span data-ttu-id="c0d27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0d27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0d27-109">*nome do servidor*</span><span class="sxs-lookup"><span data-stu-id="c0d27-109">*server-name*</span></span> 
</dt> <dd>

<span data-ttu-id="c0d27-110">Especifica o nome do servidor, ou host, computador.</span><span class="sxs-lookup"><span data-stu-id="c0d27-110">Specifies the name of the server, or host, computer.</span></span> <span data-ttu-id="c0d27-111">O nome é uma cadeia de caracteres e pode ser um nome de domínio totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="c0d27-111">The name is a character string and may be a fully qualified domain name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0d27-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0d27-112">Remarks</span></span>

<span data-ttu-id="c0d27-113">Para usar o protocolo de transporte **ncadg \_ MQ** , os componentes do MSMQ devem ser totalmente instalados e os sistemas cliente e servidor devem estar acessíveis por meio dos protocolos do MQ.</span><span class="sxs-lookup"><span data-stu-id="c0d27-113">In order to use the **ncadg\_mq** transport protocol, the MSMQ components must be fully installed and the client and server systems must be reachable through the MQ protocols.</span></span>

<span data-ttu-id="c0d27-114">O **protocolo \_ MQ ncadg** não dá suporte a pontos de extremidade dinâmicos ou chamadas de [**difusão**](broadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="c0d27-114">The **ncadg\_mq** protocol does not support dynamic endpoints or [**broadcast**](broadcast.md) calls.</span></span> <span data-ttu-id="c0d27-115">Assim como ocorre com outros protocolos de datagrama, o **ncadg \_ MQ** não oferece suporte a retornos de chamada. qualquer função que use o atributo de [**retorno de chamada**](callback.md) falhará</span><span class="sxs-lookup"><span data-stu-id="c0d27-115">As with other datagram protocols, **ncadg\_mq** does not support callbacks; any functions using the [**callback**](callback.md) attribute will fail.</span></span>

> [!Note]  
> <span data-ttu-id="c0d27-116">Não há suporte para essa família de protocolos no WindowsÂ XP.</span><span class="sxs-lookup"><span data-stu-id="c0d27-116">This protocol family is not supported in WindowsÂ XP.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c0d27-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c0d27-117">Examples</span></span>

<span data-ttu-id="c0d27-118">A sintaxe do protocolo de fila de mensagens é definida independentemente da especificação de IDL.</span><span class="sxs-lookup"><span data-stu-id="c0d27-118">The syntax of the message-queue protocol is defined independently of the IDL specification.</span></span> <span data-ttu-id="c0d27-119">O compilador MIDL executa alguma verificação de sintaxe, mas não garante que a especificação do ponto de extremidade esteja correta.</span><span class="sxs-lookup"><span data-stu-id="c0d27-119">The MIDL compiler performs some syntax checking but does not guarantee that the endpoint specification is correct.</span></span> <span data-ttu-id="c0d27-120">Alguns erros podem ser relatados em tempo de execução em vez de durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="c0d27-120">Some errors may be reported at run time rather than during compilation.</span></span>

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_mq:rainier") 
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a><span data-ttu-id="c0d27-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0d27-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d27-122">**difusor**</span><span class="sxs-lookup"><span data-stu-id="c0d27-122">**broadcast**</span></span>](broadcast.md)
</dt> <dt>

[<span data-ttu-id="c0d27-123">**retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="c0d27-123">**callback**</span></span>](callback.md)
</dt> <dt>

[<span data-ttu-id="c0d27-124">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="c0d27-124">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="c0d27-125">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="c0d27-125">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="c0d27-126">**Mensagem**</span><span class="sxs-lookup"><span data-stu-id="c0d27-126">**message**</span></span>](message.md)
</dt> <dt>

[<span data-ttu-id="c0d27-127">Enfileiramento de mensagens RPC</span><span class="sxs-lookup"><span data-stu-id="c0d27-127">RPC Message Queuing</span></span>](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[<span data-ttu-id="c0d27-128">Associação de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="c0d27-128">String Binding</span></span>](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 