---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVE para solicitar permissão para remover um dispositivo ou parte da mídia.
ms.assetid: a0e9aa57-da0e-4e9c-99d0-5502040d2664
title: DBT_DEVICEQUERYREMOVE evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b8c9dbdee13318f9a664582fdba8f9e3f9bfc5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754793"
---
# <a name="dbt_devicequeryremove-event"></a><span data-ttu-id="36dcb-103">\_Evento DBT DEVICEQUERYREMOVE</span><span class="sxs-lookup"><span data-stu-id="36dcb-103">DBT\_DEVICEQUERYREMOVE event</span></span>

<span data-ttu-id="36dcb-104">O sistema transmite o evento de \_ dispositivo DBT DEVICEQUERYREMOVE para solicitar permissão para remover um dispositivo ou parte da mídia.</span><span class="sxs-lookup"><span data-stu-id="36dcb-104">The system broadcasts the DBT\_DEVICEQUERYREMOVE device event to request permission to remove a device or piece of media.</span></span> <span data-ttu-id="36dcb-105">Essa mensagem é a última chance de aplicativos e drivers se preparar para essa remoção.</span><span class="sxs-lookup"><span data-stu-id="36dcb-105">This message is the last chance for applications and drivers to prepare for this removal.</span></span> <span data-ttu-id="36dcb-106">No entanto, qualquer aplicativo pode negar essa solicitação e cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="36dcb-106">However, any application can deny this request and cancel the operation.</span></span>

<span data-ttu-id="36dcb-107">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEQUERYREMOVE e *lParam* definido conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="36dcb-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEQUERYREMOVE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="36dcb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36dcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36dcb-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="36dcb-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="36dcb-110">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="36dcb-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="36dcb-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="36dcb-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="36dcb-112">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="36dcb-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="36dcb-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36dcb-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36dcb-114">Defina como DBT \_ DEVICEQUERYREMOVE.</span><span class="sxs-lookup"><span data-stu-id="36dcb-114">Set to DBT\_DEVICEQUERYREMOVE.</span></span>

</dd> <dt>

<span data-ttu-id="36dcb-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36dcb-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36dcb-116">Um ponteiro para uma estrutura que identifica o dispositivo a ser removido.</span><span class="sxs-lookup"><span data-stu-id="36dcb-116">A pointer to a structure identifying the device to remove.</span></span> <span data-ttu-id="36dcb-117">A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36dcb-117">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="36dcb-118">Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36dcb-118">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36dcb-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36dcb-119">Return value</span></span>

<span data-ttu-id="36dcb-120">Retornar **true** para conceder permissão para remover um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36dcb-120">Return **TRUE** to grant permission to remove a device.</span></span>

<span data-ttu-id="36dcb-121">Retornar consulta de difusão \_ \_ negar para negar permissão para remover um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="36dcb-121">Return BROADCAST\_QUERY\_DENY to deny permission to remove a device.</span></span>

## <a name="remarks"></a><span data-ttu-id="36dcb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="36dcb-122">Remarks</span></span>

<span data-ttu-id="36dcb-123">Você deve fechar todos os identificadores para o dispositivo ou a remoção do dispositivo falhará.</span><span class="sxs-lookup"><span data-stu-id="36dcb-123">You must close all handles to the device or the device removal will fail.</span></span>

## <a name="examples"></a><span data-ttu-id="36dcb-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36dcb-124">Examples</span></span>

<span data-ttu-id="36dcb-125">Para obter um exemplo, consulte [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="36dcb-125">For an example, see [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36dcb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36dcb-126">Requirements</span></span>



| <span data-ttu-id="36dcb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="36dcb-127">Requirement</span></span> | <span data-ttu-id="36dcb-128">Valor</span><span class="sxs-lookup"><span data-stu-id="36dcb-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="36dcb-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36dcb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36dcb-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="36dcb-130">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="36dcb-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36dcb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36dcb-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="36dcb-132">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="36dcb-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36dcb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="36dcb-134"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="36dcb-134"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36dcb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="36dcb-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36dcb-136">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="36dcb-136">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="36dcb-137">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="36dcb-137">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="36dcb-138">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="36dcb-138">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="36dcb-139">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="36dcb-139">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




