---
description: Solicita uma Media Foundation transformação (MFT) para que o streaming esteja prestes a terminar.
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502276"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="8c309-103">\_fim da \_ notificação de mensagem \_ de MFT \_</span><span class="sxs-lookup"><span data-stu-id="8c309-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="8c309-104">Solicita uma Media Foundation transformação (MFT) para que o streaming esteja prestes a terminar.</span><span class="sxs-lookup"><span data-stu-id="8c309-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="8c309-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="8c309-105">Message Parameter</span></span>

<span data-ttu-id="8c309-106">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="8c309-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c309-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c309-107">Remarks</span></span>

<span data-ttu-id="8c309-108">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="8c309-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="8c309-109">Não é necessário que o cliente envie essa mensagem, mesmo que o cliente tenha enviado anteriormente a mensagem de **\_ início de notificação de \_ \_ \_ transmissão de mensagem de MFT** .</span><span class="sxs-lookup"><span data-stu-id="8c309-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="8c309-110">Implementação</span><span class="sxs-lookup"><span data-stu-id="8c309-110">Implementation</span></span>

<span data-ttu-id="8c309-111">O MFT pode responder a essa mensagem liberando buffers e outros recursos.</span><span class="sxs-lookup"><span data-stu-id="8c309-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="8c309-112">O MFT não libera dados de entrada nem redefine os tipos de mídia em resposta a essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="8c309-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="8c309-113">Um MFT não é necessário para responder a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8c309-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c309-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c309-114">Requirements</span></span>



| <span data-ttu-id="8c309-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c309-115">Requirement</span></span> | <span data-ttu-id="8c309-116">Valor</span><span class="sxs-lookup"><span data-stu-id="8c309-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c309-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c309-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8c309-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c309-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8c309-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c309-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8c309-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c309-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8c309-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c309-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c309-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c309-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c309-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c309-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c309-124">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="8c309-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




