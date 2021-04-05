---
description: Gerado por um fluxo de mídia quando o tipo de mídia do fluxo é alterado.
ms.assetid: 14786a9b-413e-4fb4-b267-bfd0ccd4631b
title: Evento MEStreamFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd48e7abc8121707b150af5bc8968a50c1eb44e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827631"
---
# <a name="mestreamformatchanged-event"></a><span data-ttu-id="fe8ce-103">Evento MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="fe8ce-103">MEStreamFormatChanged event</span></span>

<span data-ttu-id="fe8ce-104">Gerado por um fluxo de mídia quando o tipo de mídia do fluxo é alterado.</span><span class="sxs-lookup"><span data-stu-id="fe8ce-104">Raised by a media stream when the media type of the stream changes.</span></span>

## <a name="event-values"></a><span data-ttu-id="fe8ce-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="fe8ce-105">Event values</span></span>

<span data-ttu-id="fe8ce-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="fe8ce-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="fe8ce-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="fe8ce-107">VARTYPE</span></span>                | <span data-ttu-id="fe8ce-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe8ce-108">Description</span></span>                                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8ce-109">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="fe8ce-109">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="fe8ce-110">Ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) do novo tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="fe8ce-110">Pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the new media type.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="fe8ce-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe8ce-111">Remarks</span></span>

<span data-ttu-id="fe8ce-112">Use esse evento para sinalizar alterações de formato no fluxo.</span><span class="sxs-lookup"><span data-stu-id="fe8ce-112">Use this event to signal format changes in the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe8ce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe8ce-113">Requirements</span></span>



| <span data-ttu-id="fe8ce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe8ce-114">Requirement</span></span> | <span data-ttu-id="fe8ce-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fe8ce-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe8ce-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe8ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe8ce-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe8ce-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fe8ce-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe8ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe8ce-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe8ce-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fe8ce-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe8ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe8ce-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe8ce-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe8ce-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe8ce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe8ce-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fe8ce-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




