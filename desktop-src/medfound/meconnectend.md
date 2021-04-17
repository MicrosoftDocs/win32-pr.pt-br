---
description: Gerado pela origem da rede quando termina de abrir uma URL.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Evento MEConnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812125"
---
# <a name="meconnectend-event"></a><span data-ttu-id="ba40f-103">Evento MEConnectEnd</span><span class="sxs-lookup"><span data-stu-id="ba40f-103">MEConnectEnd event</span></span>

<span data-ttu-id="ba40f-104">Gerado pela origem da rede quando termina de abrir uma URL.</span><span class="sxs-lookup"><span data-stu-id="ba40f-104">Raised by the network source when it finishes opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="ba40f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="ba40f-105">Event values</span></span>

<span data-ttu-id="ba40f-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ba40f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ba40f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ba40f-107">VARTYPE</span></span>              | <span data-ttu-id="ba40f-108">Description</span><span class="sxs-lookup"><span data-stu-id="ba40f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ba40f-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="ba40f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ba40f-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="ba40f-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ba40f-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba40f-111">Remarks</span></span>

<span data-ttu-id="ba40f-112">A origem da rede envia esse evento diretamente para o aplicativo por meio do método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) do aplicativo, não por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) usual.</span><span class="sxs-lookup"><span data-stu-id="ba40f-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba40f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba40f-113">Requirements</span></span>



| <span data-ttu-id="ba40f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba40f-114">Requirement</span></span> | <span data-ttu-id="ba40f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ba40f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba40f-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba40f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba40f-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba40f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ba40f-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba40f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba40f-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba40f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ba40f-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba40f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba40f-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba40f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba40f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba40f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba40f-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="ba40f-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="ba40f-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba40f-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




