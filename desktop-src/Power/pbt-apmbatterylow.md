---
description: Notifica os aplicativos que a energia da bateria está baixa.
ms.assetid: ef24b8cf-d801-4452-a03c-3f2bdbdd7e5d
title: Evento de PBT_APMBATTERYLOW (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64884f9bb01e37883e1be61b2de88862e8b119fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759352"
---
# <a name="pbt_apmbatterylow-event"></a><span data-ttu-id="1f2d0-103">\_Evento PBT APMBATTERYLOW</span><span class="sxs-lookup"><span data-stu-id="1f2d0-103">PBT\_APMBATTERYLOW event</span></span>

<span data-ttu-id="1f2d0-104">\[PBT \_ APMBATTERYLOW está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-104">\[PBT\_APMBATTERYLOW is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1f2d0-105">O suporte para esse evento foi removido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="1f2d0-106">Em vez disso, use [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) .\]</span><span class="sxs-lookup"><span data-stu-id="1f2d0-106">Use [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) instead.\]</span></span>

<span data-ttu-id="1f2d0-107">Notifica os aplicativos que a energia da bateria está baixa.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-107">Notifies applications that the battery power is low.</span></span>

<span data-ttu-id="1f2d0-108">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="1f2d0-108">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="1f2d0-109">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-109">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMBATTERYLOW
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="1f2d0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f2d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2d0-111">*HWND*</span><span class="sxs-lookup"><span data-stu-id="1f2d0-111">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="1f2d0-112">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-112">A handle to the window.</span></span>

<span data-ttu-id="1f2d0-113"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="1f2d0-113"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="1f2d0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="1f2d0-114">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="1f2d0-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1f2d0-115">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="1f2d0-116"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2d0-116"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="1f2d0-117">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-117">Message identifier.</span></span><br/> |



 

<span data-ttu-id="1f2d0-118"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="1f2d0-118"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="1f2d0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="1f2d0-119">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="1f2d0-120">Significado</span><span class="sxs-lookup"><span data-stu-id="1f2d0-120">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMBATTERYLOW"></span><span id="pbt_apmbatterylow"></span><dl> <span data-ttu-id="1f2d0-121"><dt>**PBT \_ APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2d0-121"><dt>**PBT\_APMBATTERYLOW**</dt> <dt>9 (0x9)</dt></span></span> </dl> | <span data-ttu-id="1f2d0-122">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-122">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1f2d0-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f2d0-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f2d0-124">Reservado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-124">Reserved, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2d0-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f2d0-125">Return value</span></span>

<span data-ttu-id="1f2d0-126">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f2d0-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f2d0-127">Remarks</span></span>

<span data-ttu-id="1f2d0-128">Esse evento é transmitido quando o BIOS do APM do sistema sinaliza uma notificação de baixa bateria do APM.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-128">This event is broadcast when a system's APM BIOS signals an APM battery low notification.</span></span> <span data-ttu-id="1f2d0-129">Como algumas implementações do BIOS do APM não fornecem notificações quando as baterias estão baixas, esse evento pode nunca ser transmitido em alguns computadores.</span><span class="sxs-lookup"><span data-stu-id="1f2d0-129">Because some APM BIOS implementations do not provide notifications when batteries are low, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f2d0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f2d0-130">Requirements</span></span>



| <span data-ttu-id="1f2d0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f2d0-131">Requirement</span></span> | <span data-ttu-id="1f2d0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1f2d0-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2d0-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f2d0-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2d0-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1f2d0-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f2d0-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f2d0-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2d0-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f2d0-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f2d0-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1f2d0-137">End of client support</span></span><br/>    | <span data-ttu-id="1f2d0-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1f2d0-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="1f2d0-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1f2d0-139">End of server support</span></span><br/>    | <span data-ttu-id="1f2d0-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f2d0-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="1f2d0-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f2d0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f2d0-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2d0-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f2d0-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f2d0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f2d0-144">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="1f2d0-144">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="1f2d0-145">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="1f2d0-145">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




