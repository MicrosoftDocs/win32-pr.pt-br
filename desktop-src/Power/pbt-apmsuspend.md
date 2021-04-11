---
description: Notifica os aplicativos que o computador está prestes a entrar em um estado suspenso.
ms.assetid: 61b177a0-4cff-4740-bed8-a46c06c43be8
title: Evento de PBT_APMSUSPEND (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fc6982e00565329c85e06765879b9b72b07fe6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169513"
---
# <a name="pbt_apmsuspend-event"></a><span data-ttu-id="8ffda-103">\_Evento PBT APMSUSPEND</span><span class="sxs-lookup"><span data-stu-id="8ffda-103">PBT\_APMSUSPEND event</span></span>

<span data-ttu-id="8ffda-104">Notifica os aplicativos que o computador está prestes a entrar em um estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="8ffda-104">Notifies applications that the computer is about to enter a suspended state.</span></span> <span data-ttu-id="8ffda-105">Normalmente, esse evento é transmitido quando todos os aplicativos e drivers instaláveis retornavam **verdadeiros** para um evento [PBT \_ APMQUERYSUSPEND](pbt-apmquerysuspend.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="8ffda-105">This event is typically broadcast when all applications and installable drivers have returned **TRUE** to a previous [PBT\_APMQUERYSUSPEND](pbt-apmquerysuspend.md) event.</span></span>

<span data-ttu-id="8ffda-106">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="8ffda-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="8ffda-107">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ffda-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMSUSPEND
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="8ffda-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ffda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffda-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="8ffda-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="8ffda-110">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="8ffda-110">A handle to window.</span></span>

<span data-ttu-id="8ffda-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="8ffda-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="8ffda-112">Valor</span><span class="sxs-lookup"><span data-stu-id="8ffda-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="8ffda-113">Significado</span><span class="sxs-lookup"><span data-stu-id="8ffda-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="8ffda-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffda-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="8ffda-115">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8ffda-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="8ffda-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="8ffda-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="8ffda-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8ffda-117">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="8ffda-118">Significado</span><span class="sxs-lookup"><span data-stu-id="8ffda-118">Meaning</span></span>                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMSUSPEND"></span><span id="pbt_apmsuspend"></span><dl> <span data-ttu-id="8ffda-119"><dt>**PBT \_ APMSUSPEND**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffda-119"><dt>**PBT\_APMSUSPEND**</dt> <dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="8ffda-120">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="8ffda-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8ffda-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ffda-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ffda-122">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8ffda-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffda-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ffda-123">Return value</span></span>

<span data-ttu-id="8ffda-124">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8ffda-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffda-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ffda-125">Remarks</span></span>

<span data-ttu-id="8ffda-126">Um aplicativo deve processar esse evento concluindo todas as tarefas necessárias para salvar os dados.</span><span class="sxs-lookup"><span data-stu-id="8ffda-126">An application should process this event by completing all tasks necessary to save data.</span></span>

<span data-ttu-id="8ffda-127">O sistema permite cerca de dois segundos para que um aplicativo manipule essa notificação.</span><span class="sxs-lookup"><span data-stu-id="8ffda-127">The system allows approximately two seconds for an application to handle this notification.</span></span> <span data-ttu-id="8ffda-128">Se um aplicativo ainda estiver executando operações após sua alocação de tempo expirar, o sistema poderá interromper o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8ffda-128">If an application is still performing operations after its time allotment has expired, the system may interrupt the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffda-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ffda-129">Requirements</span></span>



| <span data-ttu-id="8ffda-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ffda-130">Requirement</span></span> | <span data-ttu-id="8ffda-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8ffda-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffda-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ffda-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8ffda-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8ffda-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ffda-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ffda-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8ffda-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ffda-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8ffda-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ffda-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ffda-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ffda-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ffda-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ffda-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ffda-139">Critérios de suspensão do sistema</span><span class="sxs-lookup"><span data-stu-id="8ffda-139">System Sleep Criteria</span></span>](system-sleep-criteria.md)
</dt> <dt>

[<span data-ttu-id="8ffda-140">Eventos de ativação do sistema</span><span class="sxs-lookup"><span data-stu-id="8ffda-140">System Wake-up Events</span></span>](system-wake-up-events.md)
</dt> <dt>

[<span data-ttu-id="8ffda-141">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="8ffda-141">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="8ffda-142">PBT \_ APMQUERYSUSPEND</span><span class="sxs-lookup"><span data-stu-id="8ffda-142">PBT\_APMQUERYSUSPEND</span></span>](pbt-apmquerysuspend.md)
</dt> <dt>

[<span data-ttu-id="8ffda-143">**SetSystemPowerState**</span><span class="sxs-lookup"><span data-stu-id="8ffda-143">**SetSystemPowerState**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setsystempowerstate)
</dt> <dt>

[<span data-ttu-id="8ffda-144">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="8ffda-144">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




