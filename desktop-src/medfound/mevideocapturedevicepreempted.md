---
description: Enviado pelo IMFMediaSource que encapsula o dispositivo para indicar que o dispositivo foi admitido.
ms.assetid: 85EE663C-94B7-47EA-ABBA-A8371342EEB2
title: Evento MEVideoCaptureDevicePreempted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3968c0641d954741474b1d5ec7ffaa11dcad5f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758082"
---
# <a name="mevideocapturedevicepreempted-event"></a><span data-ttu-id="bb116-103">Evento MEVideoCaptureDevicePreempted</span><span class="sxs-lookup"><span data-stu-id="bb116-103">MEVideoCaptureDevicePreempted event</span></span>

<span data-ttu-id="bb116-104">Enviado pelo [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula o dispositivo para indicar que o dispositivo foi admitido.</span><span class="sxs-lookup"><span data-stu-id="bb116-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been preempted.</span></span>

## <a name="event-values"></a><span data-ttu-id="bb116-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="bb116-105">Event values</span></span>

<span data-ttu-id="bb116-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="bb116-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="bb116-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="bb116-107">VARTYPE</span></span>               | <span data-ttu-id="bb116-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb116-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="bb116-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="bb116-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="bb116-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="bb116-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="bb116-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb116-111">Remarks</span></span>

<span data-ttu-id="bb116-112">Esse evento é enviado pelo [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bb116-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb116-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb116-113">Requirements</span></span>



| <span data-ttu-id="bb116-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb116-114">Requirement</span></span> | <span data-ttu-id="bb116-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bb116-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb116-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb116-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bb116-117">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bb116-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="bb116-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb116-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bb116-119">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bb116-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb116-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb116-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb116-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb116-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb116-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb116-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb116-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb116-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




