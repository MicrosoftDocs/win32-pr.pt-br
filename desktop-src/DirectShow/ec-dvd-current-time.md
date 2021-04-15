---
description: Sinaliza o início de cada VOBU (unidade de objeto de vídeo), um segmento de vídeo que é de 0,4 a 1,0 segundos de comprimento.
ms.assetid: 1f2def2f-3a6b-458b-b564-09b6cf74543c
title: EC_DVD_CURRENT_TIME (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0f1bb2f5f31efa881917ac71ea381cc0a82e8744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747367"
---
# <a name="ec_dvd_current_time"></a><span data-ttu-id="522ba-103">\_ \_ hora atual do DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="522ba-103">EC\_DVD\_CURRENT\_TIME</span></span>

<span data-ttu-id="522ba-104">Sinaliza o início de cada VOBU (unidade de objeto de vídeo), um segmento de vídeo que é de 0,4 a 1,0 segundos de comprimento.</span><span class="sxs-lookup"><span data-stu-id="522ba-104">Signals the beginning of every video object unit (VOBU), a video segment which is 0.4 to 1.0 seconds in length.</span></span>

## <a name="parameters"></a><span data-ttu-id="522ba-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="522ba-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="522ba-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="522ba-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="522ba-107">Valor **DWORD** que indica o código de tempo de reprodução atual em um formato binário codificado de horas (BCD), minutos, segundos, quadros (hh: mm: SS: FF).</span><span class="sxs-lookup"><span data-stu-id="522ba-107">**DWORD** value indicating the current playback timecode in a binary coded decimal (BCD) hours, minutes, seconds, frames (HH:MM:SS:FF) format.</span></span> <span data-ttu-id="522ba-108">Membro da estrutura [**de \_ código**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) de paficação do DVD.</span><span class="sxs-lookup"><span data-stu-id="522ba-108">Member of the [**DVD\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_timecode) structure.</span></span>

</dd> <dt>

<span data-ttu-id="522ba-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="522ba-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="522ba-110">Valor booliano (**bool**) que indica o código de code.</span><span class="sxs-lookup"><span data-stu-id="522ba-110">Boolean (**BOOL**) value indicating the timecode.</span></span> <span data-ttu-id="522ba-111">Zero (0) indica 25 quadros por segundo enquanto 1 indica 30 quadros por segundo (não Descartado).</span><span class="sxs-lookup"><span data-stu-id="522ba-111">Zero (0) indicates 25 frames per second while 1 indicates 30 frames per second (nondropped).</span></span> <span data-ttu-id="522ba-112">Um valor de 2 indica que o tempo de reprodução não pode ser determinado.</span><span class="sxs-lookup"><span data-stu-id="522ba-112">A value of 2 indicates the playback time cannot be determined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="522ba-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="522ba-113">Remarks</span></span>

<span data-ttu-id="522ba-114">Somente filmes lineares simples sinalizam esse evento.</span><span class="sxs-lookup"><span data-stu-id="522ba-114">Only simple linear movies signal this event.</span></span>

<span data-ttu-id="522ba-115">Esse evento é gerado no domínio do título.</span><span class="sxs-lookup"><span data-stu-id="522ba-115">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="522ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="522ba-116">Requirements</span></span>



| <span data-ttu-id="522ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="522ba-117">Requirement</span></span> | <span data-ttu-id="522ba-118">Valor</span><span class="sxs-lookup"><span data-stu-id="522ba-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="522ba-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="522ba-119">Header</span></span><br/> | <dl> <span data-ttu-id="522ba-120"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="522ba-120"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="522ba-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="522ba-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="522ba-122">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="522ba-122">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="522ba-123">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="522ba-123">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="522ba-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="522ba-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




