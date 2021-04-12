---
description: O sistema transmite o evento de \_ dispositivo DBT DEVICEARRIVAL quando um dispositivo ou uma parte da mídia foi inserida e fica disponível.
ms.assetid: 8e44cb02-cf79-4b19-807e-20cea07362af
title: DBT_DEVICEARRIVAL evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f69c2feec996b4306c271454767ca4e75d1ff855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457014"
---
# <a name="dbt_devicearrival-event"></a><span data-ttu-id="907c4-103">\_Evento DBT DEVICEARRIVAL</span><span class="sxs-lookup"><span data-stu-id="907c4-103">DBT\_DEVICEARRIVAL event</span></span>

<span data-ttu-id="907c4-104">O sistema transmite o evento de \_ dispositivo DBT DEVICEARRIVAL quando um dispositivo ou uma parte da mídia foi inserida e fica disponível.</span><span class="sxs-lookup"><span data-stu-id="907c4-104">The system broadcasts the DBT\_DEVICEARRIVAL device event when a device or piece of media has been inserted and becomes available.</span></span>

<span data-ttu-id="907c4-105">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ DEVICEARRIVAL e *lParam* definido conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="907c4-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_DEVICEARRIVAL and *lParam* set as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="907c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="907c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="907c4-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="907c4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="907c4-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="907c4-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="907c4-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="907c4-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="907c4-110">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="907c4-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="907c4-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="907c4-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="907c4-112">Defina como DBT \_ DEVICEARRIVAL.</span><span class="sxs-lookup"><span data-stu-id="907c4-112">Set to DBT\_DEVICEARRIVAL.</span></span>

</dd> <dt>

<span data-ttu-id="907c4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="907c4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="907c4-114">Um ponteiro para uma estrutura que identifica o dispositivo inserido.</span><span class="sxs-lookup"><span data-stu-id="907c4-114">A pointer to a structure identifying the device inserted.</span></span> <span data-ttu-id="907c4-115">A estrutura consiste em um cabeçalho independente de evento, seguida por membros dependentes de evento que descrevem o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="907c4-115">The structure consists of an event-independent header, followed by event-dependent members that describe the device.</span></span> <span data-ttu-id="907c4-116">Para usar essa estrutura, trate a estrutura como uma [**estrutura \_ \_ HDR de difusão de dev**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) e, em seguida, verifique seu membro **dbch \_ DeviceType** para determinar o tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="907c4-116">To use this structure, treat the structure as a [**DEV\_BROADCAST\_HDR**](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr) structure, then check its **dbch\_devicetype** member to determine the device type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="907c4-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="907c4-117">Return value</span></span>

<span data-ttu-id="907c4-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="907c4-118">Return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="907c4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="907c4-119">Remarks</span></span>

<span data-ttu-id="907c4-120">Se a mídia estiver sendo inserida, o tipo de dispositivo que chega é um volume (o membro **dbch \_ DeviceType** é DBT \_ DEVTYP \_ volume) e a alteração afeta a mídia (o membro **\_ sinalizadores dbcv** é a \_ mídia DBTF).</span><span class="sxs-lookup"><span data-stu-id="907c4-120">If media is being inserted, the type of device arriving is a volume (the **dbch\_devicetype** member is DBT\_DEVTYP\_VOLUME) and the change effects the media (the **dbcv\_flags** member is DBTF\_MEDIA).</span></span>

## <a name="examples"></a><span data-ttu-id="907c4-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="907c4-121">Examples</span></span>

<span data-ttu-id="907c4-122">Para obter um exemplo, consulte [detectando a inserção ou remoção de mídia](detecting-media-insertion-or-removal.md).</span><span class="sxs-lookup"><span data-stu-id="907c4-122">For an example, see [Detecting Media Insertion or Removal](detecting-media-insertion-or-removal.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="907c4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="907c4-123">Requirements</span></span>



| <span data-ttu-id="907c4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="907c4-124">Requirement</span></span> | <span data-ttu-id="907c4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="907c4-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="907c4-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="907c4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="907c4-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="907c4-127">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="907c4-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="907c4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="907c4-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="907c4-129">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="907c4-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="907c4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="907c4-131"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="907c4-131"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="907c4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="907c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907c4-133">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="907c4-133">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="907c4-134">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="907c4-134">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="907c4-135">**\_cabeçalho de difusão de dev \_**</span><span class="sxs-lookup"><span data-stu-id="907c4-135">**DEV\_BROADCAST\_HDR**</span></span>](/windows/desktop/api/Dbt/ns-dbt-dev_broadcast_hdr)
</dt> <dt>

[<span data-ttu-id="907c4-136">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="907c4-136">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




