---
description: Evento de alteração de configuração de energia enviado com uma mensagem de janela do WM \_ POWERBROADCAST ou em um retorno de chamada de notificação HandlerEx para serviços.
ms.assetid: 0bcadb85-47c5-48a9-b3f9-f0a1ca60b503
title: Evento de PBT_POWERSETTINGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f38486d2e5cce1cfe541468e548e92353c9837
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828364"
---
# <a name="pbt_powersettingchange-event"></a><span data-ttu-id="d6c89-103">\_Evento PBT POWERSETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="d6c89-103">PBT\_POWERSETTINGCHANGE event</span></span>

<span data-ttu-id="d6c89-104">Evento de alteração de configuração de energia enviado com uma mensagem de janela do [**WM \_ POWERBROADCAST**](wm-powerbroadcast.md) ou em um retorno de chamada de notificação [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) para serviços.</span><span class="sxs-lookup"><span data-stu-id="d6c89-104">Power setting change event sent with a [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) window message or in a [**HandlerEx**](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) notification callback for services.</span></span>


```C++
LRESULT 
CALLBACK 
WindowProc( HWND hwnd,      // handle to window
            UINT uMsg,      // WM_POWERBROADCAST
            WPARAM wParam,  // PBT_POWERSETTINGCHANGE
            LPARAM lParam); // Pointer to POWERBROADCAST_SETTING
```



## <a name="parameters"></a><span data-ttu-id="d6c89-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6c89-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6c89-106">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d6c89-106">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c89-107">Um identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="d6c89-107">A handle to window.</span></span>

<span data-ttu-id="d6c89-108"></dd> <dt>*uMsg*</dt> </span><span class="sxs-lookup"><span data-stu-id="d6c89-108"></dd> <dt>*uMsg* </dt> </span></span><dd> 

| <span data-ttu-id="d6c89-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c89-109">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="d6c89-110">Significado</span><span class="sxs-lookup"><span data-stu-id="d6c89-110">Meaning</span></span>                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WM_POWERBROADCAST"></span><span id="wm_powerbroadcast"></span><dl> <span data-ttu-id="d6c89-111"><dt>**[**WM \_ POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span><span class="sxs-lookup"><span data-stu-id="d6c89-111"><dt>**[**WM\_POWERBROADCAST**](wm-powerbroadcast.md)**</dt> <dt>536 (0x218)</dt></span></span> </dl> | <span data-ttu-id="d6c89-112">Identificador de mensagem.</span><span class="sxs-lookup"><span data-stu-id="d6c89-112">Message identifier.</span></span><br/> |



 

<span data-ttu-id="d6c89-113"></dd> <dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="d6c89-113"></dd> <dt>*wParam* </dt> </span></span><dd> 

| <span data-ttu-id="d6c89-114">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c89-114">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="d6c89-115">Significado</span><span class="sxs-lookup"><span data-stu-id="d6c89-115">Meaning</span></span>                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| <span id="PBT_POWERSETTINGCHANGE"></span><span id="pbt_powersettingchange"></span><dl> <span data-ttu-id="d6c89-116"><dt>**PBT \_ POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span><span class="sxs-lookup"><span data-stu-id="d6c89-116"><dt>**PBT\_POWERSETTINGCHANGE**</dt> <dt>32787 (0x8013)</dt></span></span> </dl> | <span data-ttu-id="d6c89-117">Identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="d6c89-117">Event identifier.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d6c89-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6c89-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6c89-119">Ponteiro para uma estrutura de [**\_ configuração POWERBROADCAST**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) .</span><span class="sxs-lookup"><span data-stu-id="d6c89-119">Pointer to a [**POWERBROADCAST\_SETTING**](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6c89-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6c89-120">Return value</span></span>

<span data-ttu-id="d6c89-121">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d6c89-121">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6c89-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c89-122">Requirements</span></span>



| <span data-ttu-id="d6c89-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c89-123">Requirement</span></span> | <span data-ttu-id="d6c89-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c89-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c89-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6c89-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c89-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6c89-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6c89-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6c89-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c89-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6c89-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6c89-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6c89-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c89-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6c89-130"><dt>WinUser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6c89-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6c89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6c89-132">Eventos de gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="d6c89-132">Power Management Events</span></span>](power-management-events.md)
</dt> <dt>

[<span data-ttu-id="d6c89-133">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="d6c89-133">**HandlerEx**</span></span>](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex)
</dt> <dt>

[<span data-ttu-id="d6c89-134">**POWERBROADCAST do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d6c89-134">**WM\_POWERBROADCAST**</span></span>](wm-powerbroadcast.md)
</dt> <dt>

[<span data-ttu-id="d6c89-135">**configuração de POWERBROADCAST \_**</span><span class="sxs-lookup"><span data-stu-id="d6c89-135">**POWERBROADCAST\_SETTING**</span></span>](/windows/desktop/api/WinUser/ns-winuser-powerbroadcast_setting)
</dt> </dl>

 

