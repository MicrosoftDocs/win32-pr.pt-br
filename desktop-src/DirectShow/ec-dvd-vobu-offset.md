---
description: Enviado quando o navegador de DVD analisa um pacote PCI.
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
ms.openlocfilehash: 531207d4d8b0debb29dd5d02e01e400218e4a2bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779487"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="04882-103">\_Deslocamento de \_ VOBU de DVD do EC \_</span><span class="sxs-lookup"><span data-stu-id="04882-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="04882-104">Enviado quando o [navegador de DVD](dvd-navigator-filter.md) analisa um pacote PCI.</span><span class="sxs-lookup"><span data-stu-id="04882-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="04882-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="04882-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04882-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="04882-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="04882-107">O deslocamento de bloco da VOBU (unidade de objeto de vídeo mais recente).</span><span class="sxs-lookup"><span data-stu-id="04882-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="04882-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="04882-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="04882-109">O número do conjunto de títulos do vídeo atual (VTSN).</span><span class="sxs-lookup"><span data-stu-id="04882-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04882-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="04882-110">Remarks</span></span>

<span data-ttu-id="04882-111">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="04882-111">This event is disabled by default.</span></span> <span data-ttu-id="04882-112">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ EnableLoggingEvents** como **true**.</span><span class="sxs-lookup"><span data-stu-id="04882-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="04882-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04882-113">Requirements</span></span>



| <span data-ttu-id="04882-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="04882-114">Requirement</span></span> | <span data-ttu-id="04882-115">Valor</span><span class="sxs-lookup"><span data-stu-id="04882-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04882-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04882-116">Header</span></span><br/> | <dl> <span data-ttu-id="04882-117"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04882-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04882-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="04882-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04882-119">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="04882-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="04882-120">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="04882-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="04882-121">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="04882-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




