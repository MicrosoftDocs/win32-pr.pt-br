---
title: comutador/Protocol
description: A opção/Protocol especifica qual protocolo de conexão tem suporte no stub gerado.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- MIDL do comutador/Protocol
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293354"
---
# <a name="protocol-switch"></a><span data-ttu-id="7c5ce-104">comutador/Protocol</span><span class="sxs-lookup"><span data-stu-id="7c5ce-104">/protocol switch</span></span>

<span data-ttu-id="7c5ce-105">A opção **/Protocol** especifica qual protocolo de conexão tem suporte no stub gerado.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="7c5ce-106">Opções de comutação</span><span class="sxs-lookup"><span data-stu-id="7c5ce-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="7c5ce-107"><span id="dce"></span><span id="DCE"></span>DCE \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="7c5ce-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="7c5ce-108">O stub gerado dá suporte apenas ao protocolo DCE.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="7c5ce-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="7c5ce-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="7c5ce-110">O stub gerado dá suporte apenas ao protocolo Microsoft NDR64.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="7c5ce-111"><span id="all"></span><span id="ALL"></span>todos \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="7c5ce-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="7c5ce-112">O stub gerado dá suporte a todos os protocolos disponíveis para um determinado ambiente.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c5ce-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c5ce-113">Remarks</span></span>

<span data-ttu-id="7c5ce-114">O RPC realiza marshaling e desempacota os dados de acordo com um protocolo de fio estrito, também chamado de sintaxe de transferência, que define a representação de transmissão de dados, como a ordem na qual os membros de dados são empacotados, o alinhamento dos dados na transmissão, informações adicionais incluídas nos dados, entre outros.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="7c5ce-115">O Microsoft RPC é compatível com o protocolo NDR do uso DCE (representação de dados de rede).</span><span class="sxs-lookup"><span data-stu-id="7c5ce-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="7c5ce-116">Na versão de 64 bits do Windows XP, a Microsoft apresenta um NDR64 de protocolo experimental que é otimizado para transferir dados de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="7c5ce-117">NDR64 não é compatível com versões anteriores com o protocolo DCE.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="7c5ce-118">O protocolo **DCE** é compatível com a sintaxe de transferência NDR do uso DCE.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="7c5ce-119">Esse protocolo é otimizado para transferir dados de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="7c5ce-120">No momento, o protocolo **ndr64** tem suporte apenas quando usado em conjunto com a opção [**/Win64**](-win64.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5ce-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="7c5ce-121">Se um cliente somente ndr64 tentar se conectar a um servidor somente DCE, ou vice-versa, a chamada será rejeitada com o RPC \_ S \_ unsupported \_ Trans \_ SYN.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="7c5ce-122">A opção **All** cria um stub que pode usar qualquer protocolo disponível.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="7c5ce-123">Para stubs de 32 bits, o único protocolo disponível atualmente é a DCE.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="7c5ce-124">Para stubs de 64 bits, criados usando a opção [**/Win64**](-win64.md) , tanto o DCE quanto o NDR64 estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="7c5ce-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="7c5ce-125">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7c5ce-125">Examples</span></span>

<span data-ttu-id="7c5ce-126">**MIDL/Protocol All/Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="7c5ce-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="7c5ce-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c5ce-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




