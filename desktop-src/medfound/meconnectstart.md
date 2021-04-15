---
description: Gerado pela origem da rede quando ele começa a abrir uma URL.
ms.assetid: 0844ac10-cc5b-4e7f-92df-3a5901c72148
title: Evento MEConnectStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8e45d723a62854c34ba7b297e462d03fed97a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502115"
---
# <a name="meconnectstart-event"></a><span data-ttu-id="0d3f1-103">Evento MEConnectStart</span><span class="sxs-lookup"><span data-stu-id="0d3f1-103">MEConnectStart event</span></span>

<span data-ttu-id="0d3f1-104">Gerado pela origem da rede quando ele começa a abrir uma URL.</span><span class="sxs-lookup"><span data-stu-id="0d3f1-104">Raised by the network source when it starts opening a URL.</span></span>

## <a name="event-values"></a><span data-ttu-id="0d3f1-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0d3f1-105">Event values</span></span>

<span data-ttu-id="0d3f1-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0d3f1-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0d3f1-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0d3f1-107">VARTYPE</span></span>              | <span data-ttu-id="0d3f1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d3f1-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0d3f1-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="0d3f1-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0d3f1-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="0d3f1-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0d3f1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d3f1-111">Remarks</span></span>

<span data-ttu-id="0d3f1-112">A origem da rede envia esse evento diretamente para o aplicativo por meio do método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) do aplicativo, não por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) usual.</span><span class="sxs-lookup"><span data-stu-id="0d3f1-112">The network source sends this event directly to the application through the application's [**IMFSourceOpenMonitor::OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) method, not through the usual [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d3f1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d3f1-113">Requirements</span></span>



| <span data-ttu-id="0d3f1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3f1-114">Requirement</span></span> | <span data-ttu-id="0d3f1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0d3f1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3f1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d3f1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3f1-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d3f1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0d3f1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d3f1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3f1-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d3f1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0d3f1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d3f1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d3f1-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d3f1-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d3f1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d3f1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3f1-123">**IMFSourceOpenMonitor**</span><span class="sxs-lookup"><span data-stu-id="0d3f1-123">**IMFSourceOpenMonitor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[<span data-ttu-id="0d3f1-124">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d3f1-124">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




