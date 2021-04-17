---
description: Gerado por um coletor de fluxo quando a taxa é alterada.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Evento MEStreamSinkRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a26adbdb64ffd5af0896d8aebe0cef474bee9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812258"
---
# <a name="mestreamsinkratechanged-event"></a><span data-ttu-id="edd40-103">Evento MEStreamSinkRateChanged</span><span class="sxs-lookup"><span data-stu-id="edd40-103">MEStreamSinkRateChanged event</span></span>

<span data-ttu-id="edd40-104">Gerado por um coletor de fluxo quando a taxa é alterada.</span><span class="sxs-lookup"><span data-stu-id="edd40-104">Raised by a stream sink when the rate has changed.</span></span>

## <a name="event-values"></a><span data-ttu-id="edd40-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="edd40-105">Event values</span></span>

<span data-ttu-id="edd40-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="edd40-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="edd40-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="edd40-107">VARTYPE</span></span>              | <span data-ttu-id="edd40-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="edd40-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="edd40-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="edd40-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="edd40-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="edd40-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="edd40-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="edd40-111">Remarks</span></span>

<span data-ttu-id="edd40-112">Se um coletor de fluxo der suporte a alterações de taxa, ele enviará esse evento depois que a alteração de taxa for concluída.</span><span class="sxs-lookup"><span data-stu-id="edd40-112">If a stream sink supports rate changes, it sends this event after the rate change is complete.</span></span> <span data-ttu-id="edd40-113">O evento é enviado uma vez para cada chamada ao método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) do coletor.</span><span class="sxs-lookup"><span data-stu-id="edd40-113">The event is sent once for each call to the sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span> <span data-ttu-id="edd40-114">Se a alteração da taxa não for bem-sucedida, o valor do status do evento será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="edd40-114">If the rate change is not successful, the event status value is an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="edd40-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edd40-115">Requirements</span></span>



| <span data-ttu-id="edd40-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="edd40-116">Requirement</span></span> | <span data-ttu-id="edd40-117">Valor</span><span class="sxs-lookup"><span data-stu-id="edd40-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edd40-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edd40-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edd40-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="edd40-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="edd40-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edd40-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edd40-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="edd40-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="edd40-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="edd40-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="edd40-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="edd40-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edd40-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="edd40-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd40-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="edd40-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="edd40-126">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="edd40-126">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 




