---
description: MFT_MESSAGE_COMMAND_FLUSH-solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: MFT_MESSAGE_COMMAND_FLUSH (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34959303a2835e67202256341b0f5998b63d16b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092734"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="9abed-103">\_liberação de \_ comando de mensagem MFT \_</span><span class="sxs-lookup"><span data-stu-id="9abed-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="9abed-104">Solicita uma Media Foundation transformação (MFT) para liberar todos os dados armazenados.</span><span class="sxs-lookup"><span data-stu-id="9abed-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="9abed-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="9abed-105">Message Parameter</span></span>

<span data-ttu-id="9abed-106">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9abed-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="9abed-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9abed-107">Remarks</span></span>

<span data-ttu-id="9abed-108">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="9abed-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="9abed-109">Depois que essa mensagem é enviada, o MFT pode aceitar novos exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="9abed-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="9abed-110">Os tipos de mídia atuais não são invalidados.</span><span class="sxs-lookup"><span data-stu-id="9abed-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="9abed-111">Implementação</span><span class="sxs-lookup"><span data-stu-id="9abed-111">Implementation</span></span>

<span data-ttu-id="9abed-112">Todos os MFTs devem implementar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="9abed-112">All MFTs must implement this message.</span></span> <span data-ttu-id="9abed-113">Quando ele recebe essa mensagem, o MFT deve descartar qualquer amostra de mídia que esteja segurando.</span><span class="sxs-lookup"><span data-stu-id="9abed-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="9abed-114">[MFTs assíncrona](asynchronous-mfts.md): o MFT não envia outro evento [METransformNeedInput](metransformneedinput.md) até receber uma [**mensagem de \_ MFT \_ notificar \_ início \_ da \_**](mft-message-notify-start-of-stream.md) mensagem de fluxo do cliente.</span><span class="sxs-lookup"><span data-stu-id="9abed-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abed-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9abed-115">Requirements</span></span>



| <span data-ttu-id="9abed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9abed-116">Requirement</span></span> | <span data-ttu-id="9abed-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9abed-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9abed-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9abed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9abed-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9abed-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9abed-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9abed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9abed-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9abed-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9abed-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9abed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9abed-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="9abed-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abed-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9abed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abed-125">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="9abed-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




