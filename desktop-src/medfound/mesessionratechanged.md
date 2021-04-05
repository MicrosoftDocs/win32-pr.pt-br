---
description: 'Gerado pela sessão de mídia quando a taxa de reprodução é alterada. Esse evento é enviado depois que o método IMFRateControl:: SetRate é concluído de forma assíncrona.'
ms.assetid: 6bef923f-4083-46e1-9a2e-49a6825467ec
title: Evento MESessionRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4cbbd8254dfb988c94cf2016164726d578d8906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827636"
---
# <a name="mesessionratechanged-event"></a><span data-ttu-id="0ef20-104">Evento MESessionRateChanged</span><span class="sxs-lookup"><span data-stu-id="0ef20-104">MESessionRateChanged event</span></span>

<span data-ttu-id="0ef20-105">Gerado pela sessão de mídia quando a taxa de reprodução é alterada.</span><span class="sxs-lookup"><span data-stu-id="0ef20-105">Raised by the Media Session when the playback rate changes.</span></span> <span data-ttu-id="0ef20-106">Esse evento é enviado depois que o método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0ef20-106">This event is sent after the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="0ef20-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0ef20-107">Event values</span></span>

<span data-ttu-id="0ef20-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0ef20-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0ef20-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0ef20-109">VARTYPE</span></span>           | <span data-ttu-id="0ef20-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0ef20-110">Description</span></span>                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef20-111">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="0ef20-111">VT\_R4</span></span><br/> | <span data-ttu-id="0ef20-112">A nova taxa de reprodução, expressa como uma taxa da taxa de reprodução normal.</span><span class="sxs-lookup"><span data-stu-id="0ef20-112">The new playback rate, expressed as a ratio of the normal playback rate.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0ef20-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ef20-113">Requirements</span></span>



| <span data-ttu-id="0ef20-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ef20-114">Requirement</span></span> | <span data-ttu-id="0ef20-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0ef20-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef20-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ef20-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef20-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ef20-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ef20-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ef20-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef20-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ef20-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0ef20-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ef20-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef20-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ef20-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ef20-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ef20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ef20-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0ef20-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




