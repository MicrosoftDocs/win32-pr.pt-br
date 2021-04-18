---
description: 'Gerado por um fluxo de mídia quando o método IMFMediaSource:: Stop é concluído de forma assíncrona.'
ms.assetid: 80280820-b618-43d9-881e-6119dfa36e22
title: Evento MEStreamStopped (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e28060505afc6b16aa6359af21c77cf92df972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807858"
---
# <a name="mestreamstopped-event"></a><span data-ttu-id="dbc59-103">Evento MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="dbc59-103">MEStreamStopped event</span></span>

<span data-ttu-id="dbc59-104">Gerado por um fluxo de mídia quando o método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="dbc59-104">Raised by a media stream when the [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="dbc59-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="dbc59-105">Event values</span></span>

<span data-ttu-id="dbc59-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="dbc59-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="dbc59-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="dbc59-107">VARTYPE</span></span>              | <span data-ttu-id="dbc59-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="dbc59-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="dbc59-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="dbc59-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="dbc59-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="dbc59-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="dbc59-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbc59-111">Remarks</span></span>

<span data-ttu-id="dbc59-112">Cada fluxo ativo na apresentação envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="dbc59-112">Each active stream in the presentation sends this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc59-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc59-113">Requirements</span></span>



| <span data-ttu-id="dbc59-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc59-114">Requirement</span></span> | <span data-ttu-id="dbc59-115">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc59-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc59-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbc59-116">Minimum supported client</span></span><br/> | <span data-ttu-id="dbc59-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbc59-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="dbc59-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dbc59-118">Minimum supported server</span></span><br/> | <span data-ttu-id="dbc59-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbc59-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dbc59-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbc59-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="dbc59-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dbc59-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc59-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc59-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc59-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dbc59-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




