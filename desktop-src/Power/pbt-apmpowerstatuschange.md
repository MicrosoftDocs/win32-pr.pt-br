---
description: Notifica os aplicativos sobre uma alteração no status de energia do computador, como um comutador da energia da bateria para A/C.
ms.assetid: dc56fee3-e0df-4f8e-8a41-92460279280a
title: Evento de PBT_APMPOWERSTATUSCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ed67f7ba064d44614196da4190ce18a996bd5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169514"
---
# <a name="pbt_apmpowerstatuschange-event"></a><span data-ttu-id="f01d6-103">\_Evento PBT APMPOWERSTATUSCHANGE</span><span class="sxs-lookup"><span data-stu-id="f01d6-103">PBT\_APMPOWERSTATUSCHANGE event</span></span>

<span data-ttu-id="f01d6-104">Notifica os aplicativos sobre uma alteração no status de energia do computador, como um comutador da energia da bateria para A/C.</span><span class="sxs-lookup"><span data-stu-id="f01d6-104">Notifies applications of a change in the power status of the computer, such as a switch from battery power to A/C.</span></span> <span data-ttu-id="f01d6-105">O sistema também transmite esse evento quando a energia restante da bateria fica abaixo do limite especificado pelo usuário ou se a energia da bateria for alterada em um percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="f01d6-105">The system also broadcasts this event when remaining battery power slips below the threshold specified by the user or if the battery power changes by a specified percentage.</span></span>

<span data-ttu-id="f01d6-106">Uma janela recebe esse evento por meio da mensagem do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) .</span><span class="sxs-lookup"><span data-stu-id="f01d6-106">A window receives this event through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message.</span></span> <span data-ttu-id="f01d6-107">Os parâmetros *wParam* e *lParam* são definidos conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="f01d6-107">The *wParam* and *lParam* parameters are set as described following.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_APMPOWERSTATUSCHANGE
            LPARAM lParam); // zero
```



## <a name="parameters"></a><span data-ttu-id="f01d6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f01d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f01d6-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f01d6-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f01d6-110">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="f01d6-110">A handle to window.</span></span>

<span data-ttu-id="f01d6-111"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="f01d6-111"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="f01d6-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f01d6-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="f01d6-113">Significado</span><span class="sxs-lookup"><span data-stu-id="f01d6-113">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="f01d6-114"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="f01d6-114"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="f01d6-115">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f01d6-115">Message identifier.</span></span><br/> |



 

<span data-ttu-id="f01d6-116"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="f01d6-116"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="f01d6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f01d6-117">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="f01d6-118">Significado</span><span class="sxs-lookup"><span data-stu-id="f01d6-118">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_APMPOWERSTATUSCHANGE"></span><span id="pbt_apmpowerstatuschange"></span><dl> <span data-ttu-id="f01d6-119"><dt>**PBT \_ APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="f01d6-119"><dt>**PBT\_APMPOWERSTATUSCHANGE**</dt> <dt>10 (0xA)</dt></span></span> </dl> | <span data-ttu-id="f01d6-120">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="f01d6-120">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f01d6-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f01d6-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f01d6-122">Reservado deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f01d6-122">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f01d6-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f01d6-123">Return value</span></span>

<span data-ttu-id="f01d6-124">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f01d6-124">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f01d6-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f01d6-125">Remarks</span></span>

<span data-ttu-id="f01d6-126">Um aplicativo deve processar esse evento chamando a função [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar o status de energia atual do computador.</span><span class="sxs-lookup"><span data-stu-id="f01d6-126">An application should process this event by calling the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve the current power status of the computer.</span></span> <span data-ttu-id="f01d6-127">Em particular, o aplicativo deve verificar os membros **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime** e **BatteryLifePercent** da estrutura de [**\_ \_ status de energia do sistema**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) para quaisquer alterações.</span><span class="sxs-lookup"><span data-stu-id="f01d6-127">In particular, the application should check the **ACLineStatus**, **BatteryFlag**, **BatteryLifeTime**, and **BatteryLifePercent** members of the [**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) structure for any changes.</span></span> <span data-ttu-id="f01d6-128">Esse evento pode ocorrer quando a vida útil da bateria cai para menos de 5 minutos ou quando a porcentagem de vida da bateria cai abaixo de 10% ou se a vida útil da bateria for alterada em 3%.</span><span class="sxs-lookup"><span data-stu-id="f01d6-128">This event can occur when battery life drops to less than 5 minutes, or when the percentage of battery life drops below 10 percent, or if the battery life changes by 3 percent.</span></span>

## <a name="requirements"></a><span data-ttu-id="f01d6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f01d6-129">Requirements</span></span>



| <span data-ttu-id="f01d6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f01d6-130">Requirement</span></span> | <span data-ttu-id="f01d6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f01d6-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f01d6-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f01d6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f01d6-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f01d6-133">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f01d6-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f01d6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f01d6-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f01d6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f01d6-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f01d6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f01d6-137"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f01d6-137"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f01d6-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f01d6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01d6-139">Status de energia do sistema</span><span class="sxs-lookup"><span data-stu-id="f01d6-139">System Power Status</span></span>](system-power-status.md)
</dt> <dt>

[<span data-ttu-id="f01d6-140">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="f01d6-140">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="f01d6-141">**GetSystemPowerStatus**</span><span class="sxs-lookup"><span data-stu-id="f01d6-141">**GetSystemPowerStatus**</span></span>](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus)
</dt> <dt>

[<span data-ttu-id="f01d6-142">**\_status de energia do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="f01d6-142">**SYSTEM\_POWER\_STATUS**</span></span>](/windows/desktop/api/Winbase/ns-winbase-system_power_status)
</dt> <dt>

[<span data-ttu-id="f01d6-143">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f01d6-143">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> </dl>

 

 




