---
description: Gerado pela sessão de mídia quando os recursos de sessão são alterados.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766507"
---
# <a name="mesessioncapabilitieschanged-event"></a><span data-ttu-id="8e8be-103">Evento MESessionCapabilitiesChanged</span><span class="sxs-lookup"><span data-stu-id="8e8be-103">MESessionCapabilitiesChanged event</span></span>

<span data-ttu-id="8e8be-104">Gerado pela sessão de mídia quando os recursos de sessão são alterados.</span><span class="sxs-lookup"><span data-stu-id="8e8be-104">Raised by the Media Session when the session capabilities change.</span></span>

## <a name="event-values"></a><span data-ttu-id="8e8be-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="8e8be-105">Event values</span></span>

<span data-ttu-id="8e8be-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="8e8be-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="8e8be-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="8e8be-107">VARTYPE</span></span>              | <span data-ttu-id="8e8be-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e8be-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="8e8be-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="8e8be-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="8e8be-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="8e8be-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="8e8be-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e8be-111">Remarks</span></span>

<span data-ttu-id="8e8be-112">O evento contém os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e8be-112">The event contains the following attributes.</span></span>



| <span data-ttu-id="8e8be-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="8e8be-113">Attribute</span></span>                                                                     | <span data-ttu-id="8e8be-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e8be-114">Description</span></span>                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="8e8be-115">**\_SESSIONCAPS do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="8e8be-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)              | <span data-ttu-id="8e8be-116">Sinalizadores de novas funcionalidades de sessão.</span><span class="sxs-lookup"><span data-stu-id="8e8be-116">New session capabilities flags.</span></span>                  |
| [<span data-ttu-id="8e8be-117">**\_ \_ SESSIONCAPS Delta de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="8e8be-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md) | <span data-ttu-id="8e8be-118">Indica quais sinalizadores de funcionalidades foram alterados.</span><span class="sxs-lookup"><span data-stu-id="8e8be-118">Indicates which capabilities flags have changed.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="8e8be-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e8be-119">Requirements</span></span>



| <span data-ttu-id="8e8be-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e8be-120">Requirement</span></span> | <span data-ttu-id="8e8be-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8e8be-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8be-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e8be-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e8be-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e8be-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e8be-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e8be-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e8be-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e8be-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e8be-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e8be-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e8be-127"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e8be-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8be-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e8be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8be-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e8be-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




