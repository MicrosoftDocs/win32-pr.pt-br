---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICETYPESPECIFIC quando ocorre um evento específico do dispositivo.
ms.assetid: 5d68e29d-b4d7-46f4-a35e-1db286e944ca
title: DBT_DEVICETYPESPECIFIC evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d7820f5769c6edd3a48b58073b55a911dae862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826384"
---
# <a name="dbt_devicetypespecific-event"></a><span data-ttu-id="f12ad-103">\_Evento DBT DEVICETYPESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="f12ad-103">DBT\_DEVICETYPESPECIFIC event</span></span>

<span data-ttu-id="f12ad-104">O sistema transmite o evento de \_ dispositivo DBT DEVICETYPESPECIFIC quando ocorre um evento específico do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f12ad-104">The system broadcasts the DBT\_DEVICETYPESPECIFIC device event when a device-specific event occurs.</span></span>

<span data-ttu-id="f12ad-105">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICETYPESPECIFIC e *lParam* definido conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="f12ad-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICETYPESPECIFIC and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="f12ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f12ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f12ad-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="f12ad-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="f12ad-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="f12ad-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="f12ad-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="f12ad-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="f12ad-110">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="f12ad-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f12ad-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f12ad-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f12ad-112">Defina como DBT \_ DEVICETYPESPECIFIC.</span><span class="sxs-lookup"><span data-stu-id="f12ad-112">Set to DBT\_DEVICETYPESPECIFIC.</span></span>

</dd> <dt>

<span data-ttu-id="f12ad-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f12ad-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f12ad-114">Um ponteiro para uma estrutura que identifica o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f12ad-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="f12ad-115">A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f12ad-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="f12ad-116">Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f12ad-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f12ad-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f12ad-117">Return value</span></span>

<span data-ttu-id="f12ad-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="f12ad-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f12ad-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f12ad-119">Requirements</span></span>



| <span data-ttu-id="f12ad-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f12ad-120">Requirement</span></span> | <span data-ttu-id="f12ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="f12ad-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f12ad-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f12ad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f12ad-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f12ad-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="f12ad-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f12ad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f12ad-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f12ad-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f12ad-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f12ad-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f12ad-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="f12ad-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f12ad-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f12ad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f12ad-129">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f12ad-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="f12ad-130">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f12ad-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="f12ad-131">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="f12ad-131">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="f12ad-132">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="f12ad-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




