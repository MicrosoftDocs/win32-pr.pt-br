---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEREMOVECOMPLETE quando um dispositivo ou uma parte da mídia foi fisicamente removida.
ms.assetid: e25d35b9-f8f1-4850-996c-e1cb393cca66
title: DBT_DEVICEREMOVECOMPLETE evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16c899d8cee4a0be34829ba0a8edbaf27be71f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749063"
---
# <a name="dbt_deviceremovecomplete-event"></a><span data-ttu-id="b7868-103">\_Evento DBT DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="b7868-103">DBT\_DEVICEREMOVECOMPLETE event</span></span>

<span data-ttu-id="b7868-104">O sistema transmite o evento de \_ dispositivo DBT DEVICEREMOVECOMPLETE quando um dispositivo ou uma parte da mídia foi fisicamente removida.</span><span class="sxs-lookup"><span data-stu-id="b7868-104">The system broadcasts the DBT\_DEVICEREMOVECOMPLETE device event when a device or piece of media has been physically removed.</span></span>

<span data-ttu-id="b7868-105">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEREMOVECOMPLETE e *lParam* definido conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7868-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEREMOVECOMPLETE and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="b7868-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7868-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7868-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="b7868-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="b7868-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="b7868-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="b7868-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="b7868-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b7868-110">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="b7868-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b7868-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7868-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7868-112">Definir como DBT \_ DEVICEREMOVECOMPLETE</span><span class="sxs-lookup"><span data-stu-id="b7868-112">Set to DBT\_DEVICEREMOVECOMPLETE</span></span>

</dd> <dt>

<span data-ttu-id="b7868-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7868-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7868-114">Um ponteiro para uma estrutura que identifica o dispositivo removido.</span><span class="sxs-lookup"><span data-stu-id="b7868-114">A pointer to a structure identifying the device removed.</span></span> <span data-ttu-id="b7868-115">A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7868-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="b7868-116">Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b7868-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7868-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7868-117">Return value</span></span>

<span data-ttu-id="b7868-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="b7868-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7868-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7868-119">Remarks</span></span>

<span data-ttu-id="b7868-120">O sistema pode difundir uma \_ mensagem DBT DEVICEREMOVECOMPLETE sem enviar as mensagens [DBT \_ DEVICEQUERYREMOVE](dbt-devicequeryremove.md) e [DBT \_ DEVICEREMOVEPENDING](dbt-deviceremovepending.md) correspondentes.</span><span class="sxs-lookup"><span data-stu-id="b7868-120">The system may broadcast a DBT\_DEVICEREMOVECOMPLETE message without sending corresponding [DBT\_DEVICEQUERYREMOVE](dbt-devicequeryremove.md) and [DBT\_DEVICEREMOVEPENDING](dbt-deviceremovepending.md) messages.</span></span> <span data-ttu-id="b7868-121">Nesses casos, os aplicativos e os drivers devem se recuperar da perda do dispositivo da melhor maneira possível.</span><span class="sxs-lookup"><span data-stu-id="b7868-121">In such cases, the applications and drivers must recover from the loss of the device as best they can.</span></span>

<span data-ttu-id="b7868-122">Se a mídia estiver sendo removida, o tipo de dispositivo que chega é um volume (o membro **dbch \_ DeviceType** é DBT \_ DEVTYP \_ volume) e a alteração afeta a mídia (o membro **\_ sinalizadores dbcv** é a \_ mídia DBTF).</span><span class="sxs-lookup"><span data-stu-id="b7868-122">If media is being removed, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="b7868-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7868-123">Examples</span></span>

<span data-ttu-id="b7868-124">Para obter um exemplo, consulte [detectando a inserção ou remoção de mídia](detecting-media-insertion-or-removal.md) ou [processando uma solicitação para remover um dispositivo](processing-a-request-to-remove-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="b7868-124">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md) or [Processing a Request to Remove a Device](processing-a-request-to-remove-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7868-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7868-125">Requirements</span></span>



| <span data-ttu-id="b7868-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7868-126">Requirement</span></span> | <span data-ttu-id="b7868-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b7868-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b7868-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7868-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b7868-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b7868-129">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="b7868-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7868-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b7868-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b7868-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="b7868-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b7868-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7868-133"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7868-133"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7868-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7868-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7868-135">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b7868-135">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="b7868-136">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b7868-136">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="b7868-137">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="b7868-137">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="b7868-138">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="b7868-138">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




