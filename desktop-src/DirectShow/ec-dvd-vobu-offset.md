---
description: EC_DVD_VOBU_Offset-enviado quando o navegador de DVD analisa um pacote PCI.
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: EC_DVD_VOBU_Offset (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9223f2d5bb25d7b950dba8fb19c152cf3184af93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119764"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="ba64f-103">\_Deslocamento de \_ VOBU de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="ba64f-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="ba64f-104">Enviado quando o [navegador de DVD](dvd-navigator-filter.md) analisa um pacote PCI.</span><span class="sxs-lookup"><span data-stu-id="ba64f-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba64f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba64f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba64f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ba64f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ba64f-107">O deslocamento de bloco da VOBU (unidade de objeto de vídeo mais recente).</span><span class="sxs-lookup"><span data-stu-id="ba64f-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="ba64f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ba64f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ba64f-109">O número do conjunto de títulos do vídeo atual (VTSN).</span><span class="sxs-lookup"><span data-stu-id="ba64f-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba64f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba64f-110">Remarks</span></span>

<span data-ttu-id="ba64f-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="ba64f-111">This event is disabled by default.</span></span> <span data-ttu-id="ba64f-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ EnableLoggingEvents** como **true**.</span><span class="sxs-lookup"><span data-stu-id="ba64f-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba64f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba64f-113">Requirements</span></span>



| <span data-ttu-id="ba64f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba64f-114">Requirement</span></span> | <span data-ttu-id="ba64f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ba64f-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba64f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba64f-116">Header</span></span><br/> | <dl> <span data-ttu-id="ba64f-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba64f-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba64f-118">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ba64f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba64f-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="ba64f-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="ba64f-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="ba64f-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ba64f-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="ba64f-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




