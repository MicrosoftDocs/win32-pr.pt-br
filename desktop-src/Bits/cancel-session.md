---
title: Cancel-Session
description: Use o pacote Cancel-Session para encerrar a sessão de carregamento com o servidor BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- BITS DE Cancel-Session
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105755882"
---
# <a name="cancel-session"></a><span data-ttu-id="79677-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="79677-104">Cancel-Session</span></span>

<span data-ttu-id="79677-105">Use o pacote **Cancel-Session** para encerrar a sessão de carregamento com o servidor bits.</span><span class="sxs-lookup"><span data-stu-id="79677-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="79677-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="79677-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="79677-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits</span><span class="sxs-lookup"><span data-stu-id="79677-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="79677-108">Verbo específico do BITS que identifica esse pacote para o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="79677-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="79677-109">Substitua a URL remota pelo URI absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="79677-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="79677-110">Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="79677-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="79677-111">Para obter considerações sobre balanceamento de carga de rede, consulte o cabeçalho BITS-host-ID no pacote de [**criação de sessão**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="79677-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="79677-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="79677-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="79677-113">Identifica esse pacote de solicitação como um pacote Cancel-Session.</span><span class="sxs-lookup"><span data-stu-id="79677-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="79677-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão</span><span class="sxs-lookup"><span data-stu-id="79677-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="79677-115">GUID de cadeia de caracteres que identifica a sessão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="79677-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="79677-116">Substitua {GUID} pelo identificador de sessão que o servidor retorna no pacote [**ACK para a resposta de Create-Session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="79677-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="79677-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="79677-117">Remarks</span></span>

<span data-ttu-id="79677-118">Esse pacote cancelará um trabalho de carregamento se ele for enviado antes que o último fragmento seja enviado.</span><span class="sxs-lookup"><span data-stu-id="79677-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="79677-119">Cancel-Session não tem efeito em um arquivo cujo último fragmento já foi enviado.</span><span class="sxs-lookup"><span data-stu-id="79677-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="79677-120">Quando o servidor BITS recebe o último fragmento, ele grava o arquivo em seu destino final e, no caso de um upload-reply, posta o arquivo no aplicativo do servidor.</span><span class="sxs-lookup"><span data-stu-id="79677-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="79677-121">No caso de resposta de upload, o pacote de Cancel-Session cancela a parte de resposta de um trabalho de resposta de upload.</span><span class="sxs-lookup"><span data-stu-id="79677-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="79677-122">O servidor BITS libera todos os recursos e exclui todos os arquivos temporários quando recebe esse pacote.</span><span class="sxs-lookup"><span data-stu-id="79677-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="79677-123">O cliente BITS envia esse pacote quando o usuário cancela o trabalho.</span><span class="sxs-lookup"><span data-stu-id="79677-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="79677-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="79677-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79677-125">**ACK para Create-Session**</span><span class="sxs-lookup"><span data-stu-id="79677-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="79677-126">**Fechar sessão**</span><span class="sxs-lookup"><span data-stu-id="79677-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




