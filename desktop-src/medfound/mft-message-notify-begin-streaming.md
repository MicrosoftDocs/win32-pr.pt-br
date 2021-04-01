---
description: Notifica uma Media Foundation transformação (MFT) que o streaming está prestes a começar.
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164912"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="92ac5-103">notificação de mensagem de MFT \_ \_ \_ Iniciar \_ streaming</span><span class="sxs-lookup"><span data-stu-id="92ac5-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="92ac5-104">Notifica uma Media Foundation transformação (MFT) que o streaming está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="92ac5-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="92ac5-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="92ac5-105">Message Parameter</span></span>

<span data-ttu-id="92ac5-106">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="92ac5-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="92ac5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="92ac5-107">Remarks</span></span>

<span data-ttu-id="92ac5-108">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="92ac5-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="92ac5-109">O cliente não é necessário para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="92ac5-109">The client is not required to send this message.</span></span> <span data-ttu-id="92ac5-110">Se o cliente enviar essa mensagem, ele deverá fazer isso depois de definir todos os tipos de mídia no MFT e antes de chamar [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="92ac5-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="92ac5-111">O MFT pode responder alocando buffers ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="92ac5-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="92ac5-112">Se o cliente não enviar essa mensagem, o MFT alocará recursos na primeira chamada para **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="92ac5-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="92ac5-113">Portanto, o envio dessa mensagem pode reduzir a latência inicial quando o streaming começa.</span><span class="sxs-lookup"><span data-stu-id="92ac5-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="92ac5-114">Implementação</span><span class="sxs-lookup"><span data-stu-id="92ac5-114">Implementation</span></span>

<span data-ttu-id="92ac5-115">Um MFT não é necessário para responder a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="92ac5-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="92ac5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92ac5-116">Requirements</span></span>



| <span data-ttu-id="92ac5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="92ac5-117">Requirement</span></span> | <span data-ttu-id="92ac5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="92ac5-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92ac5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92ac5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92ac5-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92ac5-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="92ac5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92ac5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92ac5-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92ac5-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92ac5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92ac5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="92ac5-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ac5-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ac5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="92ac5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ac5-126">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="92ac5-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




