---
title: atributo de ponto de extremidade
description: O atributo \ Endpoint \ especifica uma porta conhecida ou portas (pontos de extremidade de comunicação) nos quais os servidores da interface escutam chamadas.
ms.assetid: b88c5a97-b726-43de-b5b6-649cda60c320
keywords:
- MIDL do atributo de ponto de extremidade
topic_type:
- apiref
api_name:
- endpoint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4383df496a791859f7249766f0dbb59266d28e93
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823688"
---
# <a name="endpoint-attribute"></a><span data-ttu-id="fafb1-104">atributo de ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="fafb1-104">endpoint attribute</span></span>

<span data-ttu-id="fafb1-105">O atributo **\[ Endpoint \]** especifica uma porta ou portas conhecidas (pontos de extremidade de comunicação) nos quais os servidores da interface escutam chamadas.</span><span class="sxs-lookup"><span data-stu-id="fafb1-105">The **\[endpoint\]** attribute specifies a well-known port or ports (communication endpoints) on which servers of the interface listen for calls.</span></span>

``` syntax
endpoint("protocol-sequence:[endpoint-port]" [ , ...] )
```

## <a name="parameters"></a><span data-ttu-id="fafb1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fafb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafb1-107">*sequência de protocolos*</span><span class="sxs-lookup"><span data-stu-id="fafb1-107">*protocol-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="fafb1-108">Especifica uma cadeia de caracteres que representa uma combinação válida de um protocolo RPC (como "ncacn"), um protocolo de transporte (como "TCP") e um protocolo de rede (como "IP").</span><span class="sxs-lookup"><span data-stu-id="fafb1-108">Specifies a character string that represents a valid combination of an RPC protocol (such as "ncacn"), a transport protocol (such as "tcp"), and a network protocol (such as "ip").</span></span> <span data-ttu-id="fafb1-109">Para obter uma lista de sequências de protocolo válidas, consulte [constantes de sequência de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="fafb1-109">For a list of valid protocol sequences, see [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

</dd> <dt>

<span data-ttu-id="fafb1-110">*ponto de extremidade-porta*</span><span class="sxs-lookup"><span data-stu-id="fafb1-110">*endpoint-port*</span></span> 
</dt> <dd>

<span data-ttu-id="fafb1-111">Especifica uma cadeia de caracteres que representa a designação do ponto de extremidade para a família de protocolos especificada.</span><span class="sxs-lookup"><span data-stu-id="fafb1-111">Specifies a string that represents the endpoint designation for the specified protocol family.</span></span> <span data-ttu-id="fafb1-112">A sintaxe da cadeia de caracteres de porta é específica para cada sequência de protocolo.</span><span class="sxs-lookup"><span data-stu-id="fafb1-112">The syntax of the port string is specific to each protocol sequence.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fafb1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fafb1-113">Remarks</span></span>

<span data-ttu-id="fafb1-114">O atributo **\[ Endpoint \]** especifica uma família de transporte, como o protocolo orientado a conexões TCP/IP, um protocolo orientado a conexões NetBIOS ou o protocolo orientado a conexão de pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="fafb1-114">The **\[endpoint\]** attribute specifies a transport family such as the TCP/IP connection-oriented protocol, a NetBIOS connection-oriented protocol, or the named-pipe connection-oriented protocol.</span></span> <span data-ttu-id="fafb1-115">O uso do atributo de **\[ ponto de extremidade \]** é consistente com outros métodos para adicionar um ponto de extremidade e não fornece serviços adicionais ou especiais para o ponto de extremidade; ele simplesmente fornece um atalho para chamar a API.</span><span class="sxs-lookup"><span data-stu-id="fafb1-115">Use of the **\[endpoint\]** attribute is consistent with other methods for adding an endpoint, and does not provide additional or special services for the endpoint; it simply provides a shortcut for calling the API.</span></span>

> [!Note]  
> <span data-ttu-id="fafb1-116">Especificar um ponto de extremidade no. A definição da interface IDL não restringe o acesso à interface para o ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="fafb1-116">Specifying an endpoint in the .IDL interface definition does not restrict access to the interface to the specified endpoint.</span></span> <span data-ttu-id="fafb1-117">Adicionando um ponto de extremidade ao. A definição de interface IDL permite que a interface seja chamada por meio de qualquer ponto de extremidade nesse processo e permite que o ponto de extremidade seja usado para chamar outras interfaces nesse processo.</span><span class="sxs-lookup"><span data-stu-id="fafb1-117">Adding an endpoint to the .IDL interface definition allows the interface to be called through any endpoint in that process, and allows the endpoint to be used to call other interfaces in that process.</span></span>

 

<span data-ttu-id="fafb1-118">O valor de *sequência de protocolo* determina os valores válidos para a porta do *ponto de extremidade*.</span><span class="sxs-lookup"><span data-stu-id="fafb1-118">The *protocol-sequence* value determines the valid values for the *endpoint-port*.</span></span> <span data-ttu-id="fafb1-119">O compilador MIDL verifica apenas a sintaxe geral para a entrada de *porta do ponto de extremidade* .</span><span class="sxs-lookup"><span data-stu-id="fafb1-119">The MIDL compiler checks only general syntax for the *endpoint-port* entry.</span></span> <span data-ttu-id="fafb1-120">Os erros de especificação de porta são relatados pelas bibliotecas de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="fafb1-120">Port specification errors are reported by the run-time libraries.</span></span> <span data-ttu-id="fafb1-121">Para obter informações sobre os valores permitidos para cada sequência de protocolo, consulte as [constantes de sequência de protocolo](/windows/desktop/Rpc/protocol-sequence-constants).</span><span class="sxs-lookup"><span data-stu-id="fafb1-121">For information about the allowed values for each protocol sequence, see the [Protocol Sequence Constants](/windows/desktop/Rpc/protocol-sequence-constants).</span></span>

<span data-ttu-id="fafb1-122">As seguintes sequências de protocolo especificadas pelo DCE não são suportadas pelo compilador MIDL fornecido com o Microsoft RPC: **ncacn \_ OSI \_ DNA** e **ncadg \_ DDS**.</span><span class="sxs-lookup"><span data-stu-id="fafb1-122">The following protocol sequences specified by DCE are not supported by the MIDL compiler provided with Microsoft RPC: **ncacn\_osi\_dna** and **ncadg\_dds**.</span></span>

<span data-ttu-id="fafb1-123">Certifique-se de ter digitado corretamente caracteres de barra invertida em pontos de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fafb1-123">Make sure that you correctly quote backslash characters in endpoints.</span></span> <span data-ttu-id="fafb1-124">Esse erro geralmente ocorre quando o ponto de extremidade é um pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="fafb1-124">This error commonly occurs when the endpoint is a named pipe.</span></span>

<span data-ttu-id="fafb1-125">As informações de ponto de extremidade especificadas no arquivo IDL são usadas pelas funções de tempo de execução RPC [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) e [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span><span class="sxs-lookup"><span data-stu-id="fafb1-125">Endpoint information specified in the IDL file is used by the RPC run-time functions [**RpcServerUseProtseqIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif) and [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif).</span></span>

## <a name="examples"></a><span data-ttu-id="fafb1-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fafb1-126">Examples</span></span>

``` syntax
endpoint("ncacn_np:[\\pipe\\rainier]") 

endpoint("ncacn_ip_tcp:[1044]", "ncacn_np:[\\pipe\\shasta]")
```

## <a name="see-also"></a><span data-ttu-id="fafb1-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fafb1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafb1-128">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="fafb1-128">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="fafb1-129">**RpcServerUseAllProtseqsIf**</span><span class="sxs-lookup"><span data-stu-id="fafb1-129">**RpcServerUseAllProtseqsIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseallprotseqsif)
</dt> <dt>

[<span data-ttu-id="fafb1-130">**RpcServerUseProtseqIf**</span><span class="sxs-lookup"><span data-stu-id="fafb1-130">**RpcServerUseProtseqIf**</span></span>](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqif)
</dt> </dl>

 

 