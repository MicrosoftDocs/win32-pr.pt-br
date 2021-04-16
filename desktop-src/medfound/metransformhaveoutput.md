---
description: Enviado por um MFT (Asynchronous Media Foundation Transformation) quando novos dados de saída estão disponíveis no MFT.
ms.assetid: a9403ad3-81bf-4cd7-ba7f-816b901bb02c
title: Evento METransformHaveOutput (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de6ee70f21c0edcf65a8090feaf90d310839749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787015"
---
# <a name="metransformhaveoutput-event"></a><span data-ttu-id="142a3-103">Evento METransformHaveOutput</span><span class="sxs-lookup"><span data-stu-id="142a3-103">METransformHaveOutput event</span></span>

<span data-ttu-id="142a3-104">Enviado por um MFT (Asynchronous Media Foundation Transformation) quando novos dados de saída estão disponíveis no MFT.</span><span class="sxs-lookup"><span data-stu-id="142a3-104">Sent by an asynchronous Media Foundation transform (MFT) when new output data is available from the MFT.</span></span>

## <a name="event-values"></a><span data-ttu-id="142a3-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="142a3-105">Event values</span></span>

<span data-ttu-id="142a3-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="142a3-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="142a3-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="142a3-107">VARTYPE</span></span>              | <span data-ttu-id="142a3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="142a3-108">Description</span></span>               |
|----------------------|---------------------------|
| <span data-ttu-id="142a3-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="142a3-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="142a3-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="142a3-110">No event data.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="142a3-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="142a3-111">Attributes</span></span>

<span data-ttu-id="142a3-112">Nenhum atributo definido para este evento.</span><span class="sxs-lookup"><span data-stu-id="142a3-112">No attributes are defined for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="142a3-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="142a3-113">Remarks</span></span>

<span data-ttu-id="142a3-114">MFTs assíncronas envie esse evento por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="142a3-114">Asynchronous MFTs send this event through the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="142a3-115">O MFTs síncrono nunca envia este evento.</span><span class="sxs-lookup"><span data-stu-id="142a3-115">Synchronous MFTs never send this event.</span></span>

<span data-ttu-id="142a3-116">Quando o cliente do MFT receber esse evento, ele deverá chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter a saída.</span><span class="sxs-lookup"><span data-stu-id="142a3-116">When the client of the MFT receives this event, it should call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get the output.</span></span>

## <a name="requirements"></a><span data-ttu-id="142a3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="142a3-117">Requirements</span></span>



| <span data-ttu-id="142a3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="142a3-118">Requirement</span></span> | <span data-ttu-id="142a3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="142a3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="142a3-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="142a3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="142a3-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="142a3-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="142a3-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="142a3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="142a3-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="142a3-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="142a3-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="142a3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="142a3-125"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="142a3-125"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142a3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="142a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142a3-127">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="142a3-127">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="142a3-128">MFTs assíncrona</span><span class="sxs-lookup"><span data-stu-id="142a3-128">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




