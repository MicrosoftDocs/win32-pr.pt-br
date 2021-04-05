---
description: Deslocamento entre o tempo de apresentação e os carimbos de data/hora das fontes de mídia.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Atributo MF_EVENT_PRESENTATION_TIME_OFFSET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827309"
---
# <a name="mf_event_presentation_time_offset-attribute"></a><span data-ttu-id="1d204-103">\_Atributo de \_ deslocamento de tempo de apresentação do evento MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="1d204-103">MF\_EVENT\_PRESENTATION\_TIME\_OFFSET attribute</span></span>

<span data-ttu-id="1d204-104">Deslocamento entre o tempo de apresentação e os carimbos de data/hora da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="1d204-104">Offset between the presentation time and the media source's time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="1d204-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="1d204-105">Data type</span></span>

<span data-ttu-id="1d204-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1d204-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="1d204-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d204-107">Remarks</span></span>

<span data-ttu-id="1d204-108">O deslocamento é calculado da seguinte maneira: offset = tempo de apresentação − hora de origem.</span><span class="sxs-lookup"><span data-stu-id="1d204-108">The offset is calculated as follows: offset = presentation time − source time.</span></span> <span data-ttu-id="1d204-109">Esse atributo é usado com os seguintes eventos:</span><span class="sxs-lookup"><span data-stu-id="1d204-109">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="1d204-110">MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="1d204-110">MESessionNotifyPresentationTime</span></span>](mesessionnotifypresentationtime.md)
-   [<span data-ttu-id="1d204-111">MESessionStarted</span><span class="sxs-lookup"><span data-stu-id="1d204-111">MESessionStarted</span></span>](mesessionstarted.md)

<span data-ttu-id="1d204-112">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1d204-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d204-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d204-113">Requirements</span></span>



| <span data-ttu-id="1d204-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d204-114">Requirement</span></span> | <span data-ttu-id="1d204-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1d204-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1d204-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d204-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d204-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1d204-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1d204-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d204-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d204-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1d204-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1d204-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d204-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d204-121"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d204-121"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d204-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d204-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d204-123">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d204-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d204-124">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="1d204-124">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="1d204-125">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="1d204-125">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="1d204-126">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="1d204-126">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




