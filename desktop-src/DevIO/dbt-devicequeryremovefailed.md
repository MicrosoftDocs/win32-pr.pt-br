---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVEFAILED quando uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.
ms.assetid: a24916a9-b67a-4622-b9f3-4b4f26bf4d6b
title: DBT_DEVICEQUERYREMOVEFAILED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848c7378cdbac95729eee70c70a1e323373b8e85
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826385"
---
# <a name="dbt_devicequeryremovefailed-event"></a><span data-ttu-id="d7ad9-103">\_Evento DBT DEVICEQUERYREMOVEFAILED</span><span class="sxs-lookup"><span data-stu-id="d7ad9-103">DBT\_DEVICEQUERYREMOVEFAILED event</span></span>

<span data-ttu-id="d7ad9-104">O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVEFAILED quando uma solicitação para remover um dispositivo ou parte da mídia foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-104">The system broadcasts the DBT\_DEVICEQUERYREMOVEFAILED device event when a request to remove a device or piece of media has been canceled.</span></span>

<span data-ttu-id="d7ad9-105">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEQUERYREMOVEFAILED e *lParam* definido conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVEFAILED and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="d7ad9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7ad9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ad9-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d7ad9-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ad9-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="d7ad9-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ad9-110">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ad9-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7ad9-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ad9-112">Defina como DBT \_ DEVICEQUERYREMOVEFAILED.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-112">Set to DBT\_DEVICEQUERYREMOVEFAILED.</span></span>

</dd> <dt>

<span data-ttu-id="d7ad9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7ad9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7ad9-114">Um ponteiro para uma estrutura que identifica o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="d7ad9-115">A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="d7ad9-116">Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ad9-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7ad9-117">Return value</span></span>

<span data-ttu-id="d7ad9-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="d7ad9-118">Return **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="d7ad9-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d7ad9-119">Examples</span></span>

<span data-ttu-id="d7ad9-120">Para obter um exemplo, consulte [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="d7ad9-120">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ad9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7ad9-121">Requirements</span></span>



| <span data-ttu-id="d7ad9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7ad9-122">Requirement</span></span> | <span data-ttu-id="d7ad9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d7ad9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d7ad9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7ad9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ad9-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d7ad9-125">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="d7ad9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7ad9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ad9-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7ad9-127">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="d7ad9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7ad9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7ad9-129"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7ad9-129"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7ad9-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7ad9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ad9-131">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7ad9-131">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="d7ad9-132">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d7ad9-132">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="d7ad9-133">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="d7ad9-133">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="d7ad9-134">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="d7ad9-134">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




