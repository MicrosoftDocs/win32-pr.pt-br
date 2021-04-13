---
description: Enviado por uma Media Foundation de transformação assíncrona (MFT) quando uma operação de descarga é concluída.
ms.assetid: 923055e5-a09a-402e-983b-6fa3cebb1b3a
title: Evento METransformDrainComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed291f9edacb11ba6edf7f5bd50a0715ae61a281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297398"
---
# <a name="metransformdraincomplete-event"></a><span data-ttu-id="bf982-103">Evento METransformDrainComplete</span><span class="sxs-lookup"><span data-stu-id="bf982-103">METransformDrainComplete event</span></span>

<span data-ttu-id="bf982-104">Enviado por uma Media Foundation de transformação assíncrona (MFT) quando uma operação de descarga é concluída.</span><span class="sxs-lookup"><span data-stu-id="bf982-104">Sent by an asynchronous Media Foundation transform (MFT) when a drain operation is complete.</span></span>

## <a name="event-values"></a><span data-ttu-id="bf982-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="bf982-105">Event values</span></span>

<span data-ttu-id="bf982-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="bf982-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bf982-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bf982-107">VARTYPE</span></span>              | <span data-ttu-id="bf982-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf982-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="bf982-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="bf982-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="bf982-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="bf982-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="bf982-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="bf982-111">Attributes</span></span>

<span data-ttu-id="bf982-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="bf982-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="bf982-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="bf982-113">Attribute</span></span>                                                                        | <span data-ttu-id="bf982-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf982-114">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="bf982-115">\_ID do \_ fluxo de entrada do MFT do evento MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="bf982-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="bf982-116">O identificador do fluxo que foi esgotado.</span><span class="sxs-lookup"><span data-stu-id="bf982-116">The identifier of the stream that was drained.</span></span><br/><span data-ttu-id="bf982-117">*Necessária*</span><span class="sxs-lookup"><span data-stu-id="bf982-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bf982-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf982-118">Remarks</span></span>

<span data-ttu-id="bf982-119">MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="bf982-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="bf982-120">O MFTs síncrono nunca envia este evento.</span><span class="sxs-lookup"><span data-stu-id="bf982-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="bf982-121">Para drenar uma MFT, chame [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem de **dreno de \_ \_ comando \_ de mensagem MFT** .</span><span class="sxs-lookup"><span data-stu-id="bf982-121">To drain an MFT, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_DRAIN** message.</span></span> <span data-ttu-id="bf982-122">Especifique o fluxo de entrada a ser esgotado no parâmetro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="bf982-122">Specify the input stream to drain in the *ulParam* parameter.</span></span> <span data-ttu-id="bf982-123">Quando a operação de descarga é concluída, um MFT assíncrono envia o evento METransformDrainComplete.</span><span class="sxs-lookup"><span data-stu-id="bf982-123">When the drain operation is completed, an asynchronous MFT sends the METransformDrainComplete event.</span></span> <span data-ttu-id="bf982-124">O atributo de [ID do fluxo de entrada do \_ MFT do evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) do evento contém o identificador de fluxo fornecido no parâmetro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="bf982-124">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event contains the stream identifier given in the *ulParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf982-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf982-125">Requirements</span></span>



| <span data-ttu-id="bf982-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf982-126">Requirement</span></span> | <span data-ttu-id="bf982-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bf982-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf982-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf982-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bf982-129">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bf982-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="bf982-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bf982-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bf982-131">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="bf982-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="bf982-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf982-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf982-133"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf982-133"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf982-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf982-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf982-135">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bf982-135">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="bf982-136">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="bf982-136">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




