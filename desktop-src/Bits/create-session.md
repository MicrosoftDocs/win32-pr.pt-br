---
title: Create-Session
description: Use o pacote Create-Session para solicitar uma sessão de carregamento com o servidor BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- BITS DE Create-Session
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453750"
---
# <a name="create-session"></a><span data-ttu-id="e1706-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="e1706-104">Create-Session</span></span>

<span data-ttu-id="e1706-105">Use o pacote **Create-Session** para solicitar uma sessão de carregamento com o servidor bits.</span><span class="sxs-lookup"><span data-stu-id="e1706-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="e1706-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="e1706-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="e1706-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits</span><span class="sxs-lookup"><span data-stu-id="e1706-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="e1706-108">Verbo específico do BITS que identifica esse pacote para o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="e1706-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="e1706-109">Substitua a URL remota pelo URI absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="e1706-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="e1706-110">Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="e1706-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="e1706-111">Para obter considerações sobre balanceamento de carga de rede, consulte o cabeçalho BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="e1706-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="e1706-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="e1706-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="e1706-113">Identifica esse pacote de solicitação como um pacote Create-Session.</span><span class="sxs-lookup"><span data-stu-id="e1706-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="e1706-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-com suporte-protocolos</span><span class="sxs-lookup"><span data-stu-id="e1706-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="e1706-115">Lista delimitada por espaço dos protocolos aos quais o cliente dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e1706-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="e1706-116">Use GUIDs de cadeia de caracteres para identificar os protocolos.</span><span class="sxs-lookup"><span data-stu-id="e1706-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="e1706-117">Especifique a lista em ordem de preferência do mais para o menos preferível.</span><span class="sxs-lookup"><span data-stu-id="e1706-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="e1706-118">A tabela a seguir lista o protocolo ao qual o cliente BITS dá suporte.</span><span class="sxs-lookup"><span data-stu-id="e1706-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="e1706-119">Substituir {guid1}... {guidn} com um ou mais GUIDs de cadeia de caracteres da lista.</span><span class="sxs-lookup"><span data-stu-id="e1706-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="e1706-120">Protocolo</span><span class="sxs-lookup"><span data-stu-id="e1706-120">Protocol</span></span>                                          | <span data-ttu-id="e1706-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="e1706-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="e1706-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span><span class="sxs-lookup"><span data-stu-id="e1706-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="e1706-123">Protocolo de upload BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="e1706-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e1706-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1706-124">Remarks</span></span>

<span data-ttu-id="e1706-125">Você deve enviar um pacote de [**ping**](ping.md) para estabelecer uma conexão http antes de enviar o pacote de Create-Session.</span><span class="sxs-lookup"><span data-stu-id="e1706-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="e1706-126">O pacote de Create-Session também pode estabelecer a conexão; no entanto, o pacote de Create-Session é menos eficiente.</span><span class="sxs-lookup"><span data-stu-id="e1706-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="e1706-127">O servidor seleciona o protocolo que deseja usar na lista que o cliente fornece no cabeçalho BITS-supported-Protocols.</span><span class="sxs-lookup"><span data-stu-id="e1706-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="e1706-128">O servidor retorna o protocolo selecionado no cabeçalho de BITS-Protocol do [**ACK para o pacote de resposta de Create-Session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="e1706-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="e1706-129">O cliente espera que o servidor retorne um [**ACK para o pacote de resposta de Create-Session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="e1706-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="e1706-130">Se o servidor foi capaz de estabelecer uma sessão, o cliente usa o pacote de solicitação de [**fragmento**](fragment.md) para enviar intervalos do arquivo para o servidor.</span><span class="sxs-lookup"><span data-stu-id="e1706-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1706-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1706-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1706-132">**ACK para Create-Session**</span><span class="sxs-lookup"><span data-stu-id="e1706-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="e1706-133">**Fragmento**</span><span class="sxs-lookup"><span data-stu-id="e1706-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="e1706-134">**Executar**</span><span class="sxs-lookup"><span data-stu-id="e1706-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





