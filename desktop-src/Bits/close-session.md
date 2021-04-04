---
title: Close-Session
description: Use o pacote Close-Session para informar ao servidor BITS que o carregamento do arquivo foi concluído e para encerrar a sessão.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- BITS DE Close-Session
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103823124"
---
# <a name="close-session"></a><span data-ttu-id="53060-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="53060-104">Close-Session</span></span>

<span data-ttu-id="53060-105">Use o pacote de **sessão de fechamento** para informar ao servidor bits que o carregamento do arquivo foi concluído e para encerrar a sessão.</span><span class="sxs-lookup"><span data-stu-id="53060-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="53060-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="53060-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="53060-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits</span><span class="sxs-lookup"><span data-stu-id="53060-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="53060-108">Verbo específico do BITS que identifica esse pacote para o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="53060-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="53060-109">Substitua a URL remota pelo URI absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="53060-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="53060-110">Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="53060-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="53060-111">Para obter considerações sobre balanceamento de carga de rede, consulte o cabeçalho BITS-host-ID no pacote de [**criação de sessão**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="53060-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="53060-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="53060-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="53060-113">Identifica esse pacote de solicitação como um pacote Close-Session.</span><span class="sxs-lookup"><span data-stu-id="53060-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="53060-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-ID da sessão</span><span class="sxs-lookup"><span data-stu-id="53060-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="53060-115">GUID de cadeia de caracteres que identifica a sessão para o servidor.</span><span class="sxs-lookup"><span data-stu-id="53060-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="53060-116">Substitua {GUID} pelo identificador de sessão que o servidor retorna no pacote [**ACK para a resposta de Create-Session**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="53060-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53060-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="53060-117">Remarks</span></span>

<span data-ttu-id="53060-118">O servidor BITS libera todos os recursos e exclui todos os arquivos temporários quando recebe esse pacote.</span><span class="sxs-lookup"><span data-stu-id="53060-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="53060-119">Para trabalhos de resposta de upload, você deve baixar a resposta antes de enviar a **sessão de fechamento**.</span><span class="sxs-lookup"><span data-stu-id="53060-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="53060-120">Caso contrário, a resposta será perdida.</span><span class="sxs-lookup"><span data-stu-id="53060-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="53060-121">Se você enviar esse pacote antes de carregar todos os fragmentos, o arquivo de carregamento será excluído; Não é possível carregar um arquivo parcial.</span><span class="sxs-lookup"><span data-stu-id="53060-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="53060-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="53060-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53060-123">**ACK para fechamento de sessão**</span><span class="sxs-lookup"><span data-stu-id="53060-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="53060-124">**Cancelar sessão**</span><span class="sxs-lookup"><span data-stu-id="53060-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="53060-125">**Criar sessão**</span><span class="sxs-lookup"><span data-stu-id="53060-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




