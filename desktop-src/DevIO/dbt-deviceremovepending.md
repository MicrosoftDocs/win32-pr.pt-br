---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEREMOVEPENDING quando um dispositivo ou parte da mídia está sendo removida e não está mais disponível para uso.
ms.assetid: 28cb4481-8961-4896-9608-afccba9a2bfe
title: DBT_DEVICEREMOVEPENDING evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421851dc46d905ae85941b92df6649ccb504ee50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089202"
---
# <a name="dbt_deviceremovepending-event"></a><span data-ttu-id="7f287-103">\_Evento DBT DEVICEREMOVEPENDING</span><span class="sxs-lookup"><span data-stu-id="7f287-103">DBT\_DEVICEREMOVEPENDING event</span></span>

<span data-ttu-id="7f287-104">O sistema transmite o evento de \_ dispositivo DBT DEVICEREMOVEPENDING quando um dispositivo ou parte da mídia está sendo removida e não está mais disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="7f287-104">The system broadcasts the DBT\_DEVICEREMOVEPENDING device event when a device or piece of media is being removed and is no longer available for use.</span></span>

<span data-ttu-id="7f287-105">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEREMOVEPENDING e *lParam* definido conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="7f287-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVEPENDING and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="7f287-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f287-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f287-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="7f287-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7f287-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="7f287-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="7f287-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="7f287-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="7f287-110">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="7f287-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7f287-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f287-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f287-112">Defina como DBT \_ DEVICEREMOVEPENDING.</span><span class="sxs-lookup"><span data-stu-id="7f287-112">Set to DBT\_DEVICEREMOVEPENDING.</span></span>

</dd> <dt>

<span data-ttu-id="7f287-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f287-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f287-114">Um ponteiro para uma estrutura que identifica o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f287-114">A pointer to a structure identifying the device.</span></span> <span data-ttu-id="7f287-115">A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f287-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="7f287-116">Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f287-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f287-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f287-117">Return value</span></span>

<span data-ttu-id="7f287-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="7f287-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f287-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f287-119">Remarks</span></span>

<span data-ttu-id="7f287-120">O sistema pode difundir uma \_ mensagem DBT DEVICEREMOVEPENDING sem enviar uma mensagem [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="7f287-120">The system may broadcast a DBT\_DEVICEREMOVEPENDING message without sending a corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) message.</span></span> <span data-ttu-id="7f287-121">Nesses casos, os aplicativos e os drivers devem se recuperar da perda do dispositivo da melhor maneira possível.</span><span class="sxs-lookup"><span data-stu-id="7f287-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

## <a name="examples"></a><span data-ttu-id="7f287-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7f287-122">Examples</span></span>

<span data-ttu-id="7f287-123">Para obter um exemplo, consulte [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="7f287-123">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7f287-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f287-124">Requirements</span></span>



| <span data-ttu-id="7f287-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f287-125">Requirement</span></span> | <span data-ttu-id="7f287-126">Valor</span><span class="sxs-lookup"><span data-stu-id="7f287-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7f287-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f287-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7f287-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f287-128">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="7f287-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f287-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7f287-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7f287-130">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="7f287-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f287-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f287-132"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f287-132"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f287-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7f287-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f287-134">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f287-134">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="7f287-135">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7f287-135">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="7f287-136">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="7f287-136">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="7f287-137">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7f287-137">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




