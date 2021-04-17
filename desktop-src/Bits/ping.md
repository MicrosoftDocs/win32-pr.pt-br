---
title: Ping
description: Use o pacote ping para estabelecer uma conexão e negociar a segurança com o servidor.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- BITS de ping
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "105753002"
---
# <a name="ping"></a><span data-ttu-id="6a34f-104">Ping</span><span class="sxs-lookup"><span data-stu-id="6a34f-104">Ping</span></span>

<span data-ttu-id="6a34f-105">Use o pacote **ping** para estabelecer uma conexão e negociar a segurança com o servidor.</span><span class="sxs-lookup"><span data-stu-id="6a34f-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="6a34f-106">Cabeçalhos</span><span class="sxs-lookup"><span data-stu-id="6a34f-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="6a34f-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_postagem de bits</span><span class="sxs-lookup"><span data-stu-id="6a34f-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="6a34f-108">Verbo específico do BITS que identifica esse pacote para o servidor BITS.</span><span class="sxs-lookup"><span data-stu-id="6a34f-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="6a34f-109">Substitua a URL remota pelo URI absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="6a34f-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="6a34f-110">Normalmente, substitua a URL remota pelo nome do arquivo remoto do trabalho.</span><span class="sxs-lookup"><span data-stu-id="6a34f-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="6a34f-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo de pacote</span><span class="sxs-lookup"><span data-stu-id="6a34f-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="6a34f-112">Identifica esse pacote de solicitação como um pacote de ping.</span><span class="sxs-lookup"><span data-stu-id="6a34f-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a34f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a34f-113">Remarks</span></span>

<span data-ttu-id="6a34f-114">O pacote de **ping** é opcional.</span><span class="sxs-lookup"><span data-stu-id="6a34f-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="6a34f-115">Em vez de enviar um pacote **ping** , você pode usar o pacote [**Create-Session**](create-session.md) para estabelecer uma conexão e negociar a segurança.</span><span class="sxs-lookup"><span data-stu-id="6a34f-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="6a34f-116">No entanto, é mais eficiente usar o pacote de **ping** para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="6a34f-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a34f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a34f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a34f-118">**ACK para ping**</span><span class="sxs-lookup"><span data-stu-id="6a34f-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="6a34f-119">**Criar sessão**</span><span class="sxs-lookup"><span data-stu-id="6a34f-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




