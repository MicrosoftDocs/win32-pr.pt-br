---
description: Enviado quando o navegador de DVD analisa um pacote PCI.
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: EC_DVD_VOBU_Timestamp (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 762a900a83154ce38ee00fcf4173ebc32b41cf30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757629"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="9569a-103">\_Carimbo de \_ \_ data/hora VOBU do EC DVD</span><span class="sxs-lookup"><span data-stu-id="9569a-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="9569a-104">Enviado quando o [navegador de DVD](dvd-navigator-filter.md) analisa um pacote PCI.</span><span class="sxs-lookup"><span data-stu-id="9569a-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="9569a-105">Os dados do evento são o carimbo de data/hora da VOBU (unidade de objeto de vídeo mais recente).</span><span class="sxs-lookup"><span data-stu-id="9569a-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="9569a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9569a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9569a-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="9569a-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="9569a-108">Contém a **DWORD** de ordem inferior do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="9569a-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="9569a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="9569a-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="9569a-110">Contém a **DWORD** de ordem superior do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="9569a-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9569a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9569a-111">Remarks</span></span>

<span data-ttu-id="9569a-112">Esse evento é desabilitado por padrão.</span><span class="sxs-lookup"><span data-stu-id="9569a-112">This event is disabled by default.</span></span> <span data-ttu-id="9569a-113">Para habilitar esse evento, chame [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e defina a opção **DVD \_ EnableLoggingEvents** como **true**.</span><span class="sxs-lookup"><span data-stu-id="9569a-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="9569a-114">Reconstrua o carimbo de data/hora da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="9569a-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="9569a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9569a-115">Requirements</span></span>



| <span data-ttu-id="9569a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9569a-116">Requirement</span></span> | <span data-ttu-id="9569a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9569a-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9569a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9569a-118">Header</span></span><br/> | <dl> <span data-ttu-id="9569a-119"><dt>Dvdevcode. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9569a-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9569a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9569a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9569a-121">Aplicativos de DVD</span><span class="sxs-lookup"><span data-stu-id="9569a-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="9569a-122">Códigos de notificação de eventos de DVD</span><span class="sxs-lookup"><span data-stu-id="9569a-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="9569a-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="9569a-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




