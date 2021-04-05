---
description: O sistema transmite o evento de \_ dispositivo DBT CONFIGCHANGECANCELED quando uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.
ms.assetid: b4b1455c-9a04-4fa0-a3fa-ed991f278c0c
title: DBT_CONFIGCHANGECANCELED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97944daa698808c55f88bc377c9bf1c59c1217fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826387"
---
# <a name="dbt_configchangecanceled-event"></a><span data-ttu-id="2097a-103">\_Evento DBT CONFIGCHANGECANCELED</span><span class="sxs-lookup"><span data-stu-id="2097a-103">DBT\_CONFIGCHANGECANCELED event</span></span>

<span data-ttu-id="2097a-104">O sistema transmite o evento de \_ dispositivo DBT CONFIGCHANGECANCELED quando uma solicitação para alterar a configuração atual (Dock ou Dock) foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="2097a-104">The system broadcasts the DBT\_CONFIGCHANGECANCELED device event when a request to change the current configuration (dock or undock) has been canceled.</span></span>

<span data-ttu-id="2097a-105">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ CONFIGCHANGECANCELED e *lParam* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="2097a-105">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGECANCELED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="2097a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2097a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2097a-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="2097a-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2097a-108">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="2097a-108">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="2097a-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="2097a-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2097a-110">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="2097a-110">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2097a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2097a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2097a-112">Defina como DBT \_ CONFIGCHANGECANCELED.</span><span class="sxs-lookup"><span data-stu-id="2097a-112">Set to DBT\_CONFIGCHANGECANCELED.</span></span>

</dd> <dt>

<span data-ttu-id="2097a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2097a-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2097a-114">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="2097a-114">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2097a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2097a-115">Return value</span></span>

<span data-ttu-id="2097a-116">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="2097a-116">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2097a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2097a-117">Requirements</span></span>



| <span data-ttu-id="2097a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2097a-118">Requirement</span></span> | <span data-ttu-id="2097a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2097a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2097a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2097a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2097a-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2097a-121">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="2097a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2097a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2097a-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2097a-123">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="2097a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2097a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2097a-125"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2097a-125"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2097a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2097a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2097a-127">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2097a-127">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="2097a-128">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2097a-128">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="2097a-129">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2097a-129">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




