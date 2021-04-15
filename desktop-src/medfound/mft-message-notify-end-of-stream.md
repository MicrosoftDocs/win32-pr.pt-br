---
description: Notifica uma Media Foundation transformação (MFT) que um fluxo de entrada terminou.
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761660"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="cfabc-103">\_ \_ \_ fim \_ da notificação de \_ mensagem MFT</span><span class="sxs-lookup"><span data-stu-id="cfabc-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="cfabc-104">Notifica uma Media Foundation transformação (MFT) que um fluxo de entrada terminou.</span><span class="sxs-lookup"><span data-stu-id="cfabc-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="cfabc-105">Parâmetro de mensagem</span><span class="sxs-lookup"><span data-stu-id="cfabc-105">Message Parameter</span></span>

<span data-ttu-id="cfabc-106">O parâmetro *ulParam* contém o identificador do fluxo de entrada, especificado como um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="cfabc-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="cfabc-107">Em aplicativos de 64 bits, coloque esse valor no menor 32 bits do **ULONG \_ PTR**.</span><span class="sxs-lookup"><span data-stu-id="cfabc-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfabc-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfabc-108">Remarks</span></span>

<span data-ttu-id="cfabc-109">Para enviar esta mensagem, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span><span class="sxs-lookup"><span data-stu-id="cfabc-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="cfabc-110">O cliente não é necessário para enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="cfabc-110">The client is not required to send this message.</span></span>

<span data-ttu-id="cfabc-111">Depois que um fluxo termina, o cliente pode chamar [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) novamente para enviar novos dados para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfabc-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="cfabc-112">Nesse caso, o cliente deve definir o atributo de descontinuidade (atributo de [**\_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) ) no primeiro exemplo de entrada após o término do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfabc-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="cfabc-113">(O cliente sempre deve definir esse atributo no primeiro exemplo novo após o término de um fluxo, independentemente de o cliente ter enviado a mensagem **\_ \_ \_ de fim \_ de notificação de fim de \_ transmissão da mensagem do MFT** .</span><span class="sxs-lookup"><span data-stu-id="cfabc-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="cfabc-114">Para obter mais informações sobre como tratar descontinuidades, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).)</span><span class="sxs-lookup"><span data-stu-id="cfabc-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="cfabc-115">Depois de enviar essa mensagem para cada fluxo de entrada, o cliente normalmente envia um comando de **\_ dreno de \_ comando \_ de mensagem MFT** e, em seguida, coleta a saída restante.</span><span class="sxs-lookup"><span data-stu-id="cfabc-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="cfabc-116">No entanto, o cliente não precisa drenar o MFT.</span><span class="sxs-lookup"><span data-stu-id="cfabc-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="cfabc-117">Se o cliente não drenar o MFT, o MFT normalmente descartará os dados não processados na próxima chamada para [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), quando detectar a descontinuidade do fluxo.</span><span class="sxs-lookup"><span data-stu-id="cfabc-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="cfabc-118">Como alternativa, o cliente pode liberar o MFT antes de chamar **ProcessInput**.</span><span class="sxs-lookup"><span data-stu-id="cfabc-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="cfabc-119">Essa mensagem não remove o fluxo de entrada ou redefine o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cfabc-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="cfabc-120">Implementação</span><span class="sxs-lookup"><span data-stu-id="cfabc-120">Implementation</span></span>

<span data-ttu-id="cfabc-121">Um MFT não é necessário para responder a esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="cfabc-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfabc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfabc-122">Requirements</span></span>



| <span data-ttu-id="cfabc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfabc-123">Requirement</span></span> | <span data-ttu-id="cfabc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cfabc-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfabc-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfabc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="cfabc-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfabc-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cfabc-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfabc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="cfabc-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cfabc-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cfabc-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfabc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfabc-130"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfabc-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfabc-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfabc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfabc-132">**\_tipo de mensagem MFT \_**</span><span class="sxs-lookup"><span data-stu-id="cfabc-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




