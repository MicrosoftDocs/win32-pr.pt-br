---
description: Enviado por uma Media Foundation de transformação assíncrona (MFT) em resposta a uma \_ mensagem de marcador de comando de mensagem MFT \_ \_ .
ms.assetid: d0c0d62d-9133-4d4b-8606-c2ae1d4c9f0a
title: Evento METransformMarker (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab79c47e2ddb26f2366aff075548f7905807df1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757716"
---
# <a name="metransformmarker-event"></a><span data-ttu-id="f4c40-103">Evento METransformMarker</span><span class="sxs-lookup"><span data-stu-id="f4c40-103">METransformMarker event</span></span>

<span data-ttu-id="f4c40-104">Enviado por uma Media Foundation de transformação assíncrona (MFT) em resposta a uma mensagem de **\_ marcador de \_ comando \_ de mensagem MFT** .</span><span class="sxs-lookup"><span data-stu-id="f4c40-104">Sent by an asynchronous Media Foundation transform (MFT) in response to an **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span>

## <a name="event-values"></a><span data-ttu-id="f4c40-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="f4c40-105">Event values</span></span>

<span data-ttu-id="f4c40-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="f4c40-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="f4c40-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="f4c40-107">VARTYPE</span></span>              | <span data-ttu-id="f4c40-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4c40-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="f4c40-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="f4c40-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="f4c40-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="f4c40-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f4c40-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="f4c40-111">Attributes</span></span>

<span data-ttu-id="f4c40-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="f4c40-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="f4c40-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="f4c40-113">Attribute</span></span>                                                      | <span data-ttu-id="f4c40-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4c40-114">Description</span></span>                                                                                                                |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c40-115">\_contexto de \_ MFT do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="f4c40-115">MF\_EVENT\_MFT\_CONTEXT</span></span>](mf-event-mft-context.md)<br/> | <span data-ttu-id="f4c40-116">O valor do parâmetro *ulParam* da mensagem do **\_ marcador de \_ comando \_ da mensagem MFT** .</span><span class="sxs-lookup"><span data-stu-id="f4c40-116">The value of the *ulParam* parameter from the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span><br/><span data-ttu-id="f4c40-117">*Necessária*</span><span class="sxs-lookup"><span data-stu-id="f4c40-117">*(Required)*</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f4c40-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4c40-118">Remarks</span></span>

<span data-ttu-id="f4c40-119">MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="f4c40-119">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="f4c40-120">O MFTs síncrono nunca envia este evento.</span><span class="sxs-lookup"><span data-stu-id="f4c40-120">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="f4c40-121">O cliente de uma MFT assíncrona pode inserir um marcador no fluxo chamando [**IMFTransform::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) com a mensagem **do \_ \_ \_ marcador de comando de mensagem MFT** .</span><span class="sxs-lookup"><span data-stu-id="f4c40-121">The client of an asynchronous MFT can place a marker in the stream by calling [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) with the **MFT\_MESSAGE\_COMMAND\_MARKER** message.</span></span> <span data-ttu-id="f4c40-122">O parâmetro *ulParam* contém dados definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f4c40-122">The *ulParam* parameter contains application-defined data.</span></span>

<span data-ttu-id="f4c40-123">Quando o MFT termina de processar todos os dados de entrada que estavam disponíveis no momento da chamada [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) , o MFT enfileira um evento METransformMarker.</span><span class="sxs-lookup"><span data-stu-id="f4c40-123">When the MFT finishes processing all of the input data that was available at the time of the [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) call, the MFT queues an METransformMarker event.</span></span> <span data-ttu-id="f4c40-124">O atributo de [contexto de \_ MFT do evento \_ \_ MF](mf-event-mft-context.md) do evento contém o valor do parâmetro *ulParam* .</span><span class="sxs-lookup"><span data-stu-id="f4c40-124">The [MF\_EVENT\_MFT\_CONTEXT](mf-event-mft-context.md) attribute of the event contains the value of the *ulParam* parameter.</span></span> <span data-ttu-id="f4c40-125">Para obter mais informações, consulte [assíncrona MFTs](asynchronous-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="f4c40-125">For more information, see [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c40-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4c40-126">Requirements</span></span>



| <span data-ttu-id="f4c40-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c40-127">Requirement</span></span> | <span data-ttu-id="f4c40-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f4c40-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c40-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4c40-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c40-130">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f4c40-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="f4c40-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4c40-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c40-132">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f4c40-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="f4c40-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4c40-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4c40-134"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4c40-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4c40-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4c40-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c40-136">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4c40-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f4c40-137">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="f4c40-137">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




