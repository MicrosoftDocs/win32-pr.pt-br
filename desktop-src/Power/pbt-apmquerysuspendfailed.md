---
description: Notifica os aplicativos que a permissão para suspender o computador foi negada.
ms.assetid: 0f68628f-9d38-45ca-9487-95bf62075e00
title: Evento de PBT_APMQUERYSUSPENDFAILED (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1544cd5ed94ae0228c739e2ddb576b0bd77146eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759616"
---
# <a name="pbt_apmquerysuspendfailed-event"></a><span data-ttu-id="bb5ea-103">\_Evento PBT APMQUERYSUSPENDFAILED</span><span class="sxs-lookup"><span data-stu-id="bb5ea-103">PBT\_APMQUERYSUSPENDFAILED event</span></span>

<span data-ttu-id="bb5ea-104">\[PBT \_ APMQUERYSUSPENDFAILED está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-104">\[PBT\_APMQUERYSUSPENDFAILED is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bb5ea-105">O suporte para esse evento foi removido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-105">Support for this event was removed in Windows Vista.</span></span> <span data-ttu-id="bb5ea-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="bb5ea-106">Use [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) instead.\]</span></span>

<span data-ttu-id="bb5ea-107">Notifica os aplicativos que a permissão para suspender o computador foi negada.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-107">Notifies applications that permission to suspend the computer was denied.</span></span> <span data-ttu-id="bb5ea-108">Esse evento será transmitido se qualquer aplicativo ou driver retornasse uma **consulta de difusão \_ \_ negada** a um evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-108">This event is broadcast if any application or driver returned **BROADCAST\_QUERY\_DENY** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="bb5ea-109">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5ea-109">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="bb5ea-110">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-110">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND   hwnd,    // handle to window
            UINT   uMsg,    // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMQUERYSUSPENDFAILED
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="bb5ea-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb5ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb5ea-112">*HWND*</span><span class="sxs-lookup"><span data-stu-id="bb5ea-112">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5ea-113">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-113">A handle to window.</span></span>

<span data-ttu-id="bb5ea-114"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="bb5ea-114"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="bb5ea-115">Valor</span><span class="sxs-lookup"><span data-stu-id="bb5ea-115">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="bb5ea-116">Significado</span><span class="sxs-lookup"><span data-stu-id="bb5ea-116">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="bb5ea-117"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ea-117"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="bb5ea-118">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-118">Message identifier.</span></span><br/> |



 

<span data-ttu-id="bb5ea-119"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="bb5ea-119"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="bb5ea-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bb5ea-120">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="bb5ea-121">Significado</span><span class="sxs-lookup"><span data-stu-id="bb5ea-121">Meaning</span></span>                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMQUERYSUSPENDFAILED"></span><span id="pbt_apmquerysuspendfailed"></span><dl> <span data-ttu-id="bb5ea-122"><dt>**PBT \_ APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ea-122"><dt>**PBT\_APMQUERYSUSPENDFAILED**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="bb5ea-123">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-123">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bb5ea-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb5ea-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb5ea-125">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-125">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb5ea-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb5ea-126">Return value</span></span>

<span data-ttu-id="bb5ea-127">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-127">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb5ea-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb5ea-128">Remarks</span></span>

<span data-ttu-id="bb5ea-129">Normalmente, os aplicativos respondem a esse evento retomando a operação normal.</span><span class="sxs-lookup"><span data-stu-id="bb5ea-129">Applications typically respond to this event by resuming normal operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb5ea-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb5ea-130">Requirements</span></span>



| <span data-ttu-id="bb5ea-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5ea-131">Requirement</span></span> | <span data-ttu-id="bb5ea-132">Valor</span><span class="sxs-lookup"><span data-stu-id="bb5ea-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5ea-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb5ea-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bb5ea-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bb5ea-134">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bb5ea-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb5ea-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bb5ea-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb5ea-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb5ea-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bb5ea-137">End of client support</span></span><br/>    | <span data-ttu-id="bb5ea-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bb5ea-138">Windows XP</span></span><br/>                                                                                    |
| <span data-ttu-id="bb5ea-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="bb5ea-139">End of server support</span></span><br/>    | <span data-ttu-id="bb5ea-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bb5ea-140">Windows Server 2003</span></span><br/>                                                                           |
| <span data-ttu-id="bb5ea-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb5ea-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb5ea-142"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bb5ea-142"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5ea-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb5ea-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5ea-144">Gerenciamento de Energia</span><span class="sxs-lookup"><span data-stu-id="bb5ea-144">Power Management</span></span>](power-management-portal.md)
</dt> <dt>

[<span data-ttu-id="bb5ea-145">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="bb5ea-145">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="bb5ea-146">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="bb5ea-146">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="bb5ea-147">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bb5ea-147">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




