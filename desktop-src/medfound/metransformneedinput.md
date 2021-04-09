---
description: Enviado por uma Media Foundation de transformação assíncrona (MFT) para solicitar um novo exemplo de entrada.
ms.assetid: 5d5c50d9-fe4e-47ff-ae09-980911ebfb22
title: Evento METransformNeedInput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63cbdea648e4dc7d90b1321958eebb6c544ebb88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090699"
---
# <a name="metransformneedinput-event"></a><span data-ttu-id="e7ed4-103">Evento METransformNeedInput</span><span class="sxs-lookup"><span data-stu-id="e7ed4-103">METransformNeedInput event</span></span>

<span data-ttu-id="e7ed4-104">Enviado por uma Media Foundation de transformação assíncrona (MFT) para solicitar um novo exemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-104">Sent by an asynchronous Media Foundation transform (MFT) to request a new input sample.</span></span>

## <a name="event-values"></a><span data-ttu-id="e7ed4-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="e7ed4-105">Event values</span></span>

<span data-ttu-id="e7ed4-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="e7ed4-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="e7ed4-107">VARTYPE</span></span>              | <span data-ttu-id="e7ed4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7ed4-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="e7ed4-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="e7ed4-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="e7ed4-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="e7ed4-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="e7ed4-111">Attributes</span></span>

<span data-ttu-id="e7ed4-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="e7ed4-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="e7ed4-113">Attribute</span></span>                                                                        | <span data-ttu-id="e7ed4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7ed4-114">Description</span></span>                                                                           |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7ed4-115">\_ID do \_ fluxo de entrada do MFT do evento MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e7ed4-115">MF\_EVENT\_MFT\_INPUT\_STREAM\_ID</span></span>](mf-event-mft-input-stream-id.md)<br/> | <span data-ttu-id="e7ed4-116">O identificador do fluxo que precisa de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-116">The identifier of the stream that needs input data.</span></span><br/><span data-ttu-id="e7ed4-117">*Necessária*</span><span class="sxs-lookup"><span data-stu-id="e7ed4-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7ed4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7ed4-118">Remarks</span></span>

<span data-ttu-id="e7ed4-119">MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="e7ed4-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="e7ed4-120">O MFTs síncrono nunca envia este evento.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="e7ed4-121">Quando o cliente do MFT receber esse evento, ele deverá chamar [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) para entregar o próximo exemplo.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-121">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) to deliver the next sample.</span></span> <span data-ttu-id="e7ed4-122">O atributo de [ID do fluxo de entrada do \_ MFT do evento \_ \_ \_ \_ MF](mf-event-mft-input-stream-id.md) do objeto de evento especifica qual fluxo de entrada requer dados.</span><span class="sxs-lookup"><span data-stu-id="e7ed4-122">The [MF\_EVENT\_MFT\_INPUT\_STREAM\_ID](mf-event-mft-input-stream-id.md) attribute of the event object specifies which input stream requires data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7ed4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7ed4-123">Requirements</span></span>



| <span data-ttu-id="e7ed4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7ed4-124">Requirement</span></span> | <span data-ttu-id="e7ed4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e7ed4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7ed4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7ed4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e7ed4-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7ed4-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e7ed4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7ed4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e7ed4-129">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="e7ed4-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="e7ed4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7ed4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7ed4-131"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7ed4-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7ed4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7ed4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ed4-133">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7ed4-133">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="e7ed4-134">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="e7ed4-134">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




