---
description: Notifica os aplicativos que o BIOS do APM sinalizou um evento de OEM do APM.
ms.assetid: 3251ac00-41f1-44e9-a579-fa31e7c7d2ff
title: Evento de PBT_APMOEMEVENT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a99b99bdaf69b1a53a24ad33cd898fd1c806694
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769295"
---
# <a name="pbt_apmoemevent-event"></a><span data-ttu-id="3e234-103">\_Evento PBT APMOEMEVENT</span><span class="sxs-lookup"><span data-stu-id="3e234-103">PBT\_APMOEMEVENT event</span></span>

<span data-ttu-id="3e234-104">\[PBT \_ APMOEMEVENT está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3e234-104">\[PBT\_APMOEMEVENT is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e234-105">O suporte para esse evento foi removido no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="3e234-105">Support for this event was removed in Windows Vista.\]</span></span>

<span data-ttu-id="3e234-106">Notifica os aplicativos que o BIOS do APM sinalizou um evento de OEM do APM.</span><span class="sxs-lookup"><span data-stu-id="3e234-106">Notifies applications that the APM BIOS has signaled an APM OEM event.</span></span>

<span data-ttu-id="3e234-107">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="3e234-107">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="3e234-108">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e234-108">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMOEMEVENT
            LPARAM lParam); // OEM event code
```



## <a name="parameters"></a><span data-ttu-id="3e234-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e234-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e234-110">*HWND*</span><span class="sxs-lookup"><span data-stu-id="3e234-110">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="3e234-111">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="3e234-111">A handle to window.</span></span>

<span data-ttu-id="3e234-112"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="3e234-112"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="3e234-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3e234-113">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="3e234-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3e234-114">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="3e234-115"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="3e234-115"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="3e234-116">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="3e234-116">Message identifier.</span></span><br/> |



 

<span data-ttu-id="3e234-117"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="3e234-117"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="3e234-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3e234-118">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="3e234-119">Significado</span><span class="sxs-lookup"><span data-stu-id="3e234-119">Meaning</span></span>                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMOEMEVENT"></span><span id="pbt_apmoemevent"></span><dl> <span data-ttu-id="3e234-120"><dt>**PBT \_ APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="3e234-120"><dt>**PBT\_APMOEMEVENT**</dt> <dt>11 (0xB)</dt></span></span> </dl> | <span data-ttu-id="3e234-121">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="3e234-121">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3e234-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e234-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e234-123">O código de evento definido pelo OEM que foi sinalizado pelo BIOS do APM do sistema.</span><span class="sxs-lookup"><span data-stu-id="3e234-123">The OEM-defined event code that was signaled by the system's APM BIOS.</span></span> <span data-ttu-id="3e234-124">Os códigos de evento OEM estão no intervalo 0200h-02FFh.</span><span class="sxs-lookup"><span data-stu-id="3e234-124">OEM event codes are in the range 0200h - 02FFh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e234-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e234-125">Return value</span></span>

<span data-ttu-id="3e234-126">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="3e234-126">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e234-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e234-127">Remarks</span></span>

<span data-ttu-id="3e234-128">Como nem todas as implementações do BIOS do APM fornecem notificações de eventos do OEM, esse evento pode nunca ser transmitido em alguns computadores.</span><span class="sxs-lookup"><span data-stu-id="3e234-128">Because not all APM BIOS implementations provide OEM event notifications, this event may never be broadcast on some computers.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e234-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e234-129">Requirements</span></span>



| <span data-ttu-id="3e234-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e234-130">Requirement</span></span> | <span data-ttu-id="3e234-131">Valor</span><span class="sxs-lookup"><span data-stu-id="3e234-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e234-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e234-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3e234-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3e234-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3e234-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e234-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3e234-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e234-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e234-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3e234-136">End of client support</span></span><br/>    | <span data-ttu-id="3e234-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e234-137">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="3e234-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3e234-138">End of server support</span></span><br/>    | <span data-ttu-id="3e234-139">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e234-139">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="3e234-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e234-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e234-141"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e234-141"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e234-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e234-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e234-143">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="3e234-143">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="3e234-144">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3e234-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




