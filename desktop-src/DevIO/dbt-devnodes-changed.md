---
description: O sistema transmite o evento de \_ dispositivo DBT DEVNODES \_ alterado quando um dispositivo foi adicionado ou removido do sistema. Os aplicativos que mantêm listas de dispositivos no sistema devem atualizar suas listas.
ms.assetid: 62acc633-7dad-4792-a5a2-1f95356479d1
title: DBT_DEVNODES_CHANGED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1450e9a87d541e5df3d9a9286e48601697e6aaae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089201"
---
# <a name="dbt_devnodes_changed-event"></a><span data-ttu-id="a972d-104">Evento de alteração de DBT \_ DEVNODES \_</span><span class="sxs-lookup"><span data-stu-id="a972d-104">DBT\_DEVNODES\_CHANGED event</span></span>

<span data-ttu-id="a972d-105">O sistema transmite o evento de \_ dispositivo DBT DEVNODES \_ alterado quando um dispositivo foi adicionado ou removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a972d-105">The system broadcasts the DBT\_DEVNODES\_CHANGED device event when a device has been added to or removed from the system.</span></span> <span data-ttu-id="a972d-106">Os aplicativos que mantêm listas de dispositivos no sistema devem atualizar suas listas.</span><span class="sxs-lookup"><span data-stu-id="a972d-106">Applications that maintain lists of devices in the system should refresh their lists.</span></span>

<span data-ttu-id="a972d-107">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVNODES \_ alterado e *lParam* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a972d-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVNODES\_CHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="a972d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a972d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a972d-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="a972d-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="a972d-110">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="a972d-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="a972d-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="a972d-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="a972d-112">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="a972d-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a972d-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a972d-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a972d-114">Definido como DBT \_ DEVNODES \_ foi alterado.</span><span class="sxs-lookup"><span data-stu-id="a972d-114">Set to DBT\_DEVNODES\_CHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="a972d-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a972d-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a972d-116">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a972d-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a972d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a972d-117">Return value</span></span>

<span data-ttu-id="a972d-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="a972d-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a972d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a972d-119">Remarks</span></span>

<span data-ttu-id="a972d-120">Não há informações adicionais sobre qual dispositivo foi adicionado ou removido do sistema.</span><span class="sxs-lookup"><span data-stu-id="a972d-120">There is no additional information about which device has been added to or removed from the system.</span></span> <span data-ttu-id="a972d-121">Os aplicativos que exigem mais informações devem se registrar para a notificação do dispositivo usando a função [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) .</span><span class="sxs-lookup"><span data-stu-id="a972d-121">Applications that require more information should register for device notification using the [**RegisterDeviceNotification**](/windows/desktop/api/Winuser/nf-winuser-registerdevicenotificationa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a972d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a972d-122">Requirements</span></span>



| <span data-ttu-id="a972d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a972d-123">Requirement</span></span> | <span data-ttu-id="a972d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="a972d-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a972d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a972d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a972d-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a972d-126">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="a972d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a972d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a972d-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a972d-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="a972d-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a972d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a972d-130"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a972d-130"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a972d-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a972d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a972d-132">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a972d-132">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="a972d-133">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a972d-133">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="a972d-134">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="a972d-134">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="a972d-135">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a972d-135">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




