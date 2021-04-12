---
description: O sistema transmite o evento de \_ dispositivo DBT QUERYCHANGECONFIG para solicitar permissão para alterar a configuração atual (Dock ou desencaixar). Qualquer aplicativo pode negar essa solicitação e cancelar a alteração.
ms.assetid: 2e452ea7-e2bf-4500-952a-ee7d891533a0
title: DBT_QUERYCHANGECONFIG evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48367da1788ae2985b21fad6e960153008e9ffd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500950"
---
# <a name="dbt_querychangeconfig-event"></a><span data-ttu-id="03d98-104">\_Evento DBT QUERYCHANGECONFIG</span><span class="sxs-lookup"><span data-stu-id="03d98-104">DBT\_QUERYCHANGECONFIG event</span></span>

<span data-ttu-id="03d98-105">O sistema transmite o evento de \_ dispositivo DBT QUERYCHANGECONFIG para solicitar permissão para alterar a configuração atual (Dock ou desencaixar).</span><span class="sxs-lookup"><span data-stu-id="03d98-105">The system broadcasts the DBT\_QUERYCHANGECONFIG device event to request permission to change the current configuration (dock or undock).</span></span> <span data-ttu-id="03d98-106">Qualquer aplicativo pode negar essa solicitação e cancelar a alteração.</span><span class="sxs-lookup"><span data-stu-id="03d98-106">Any application can deny this request and cancel the change.</span></span>

<span data-ttu-id="03d98-107">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ QUERYCHANGECONFIG e *lParam* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="03d98-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_QUERYCHANGECONFIG and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="03d98-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03d98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03d98-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="03d98-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="03d98-110">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="03d98-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="03d98-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="03d98-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="03d98-112">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="03d98-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="03d98-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03d98-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03d98-114">Defina como DBT \_ QUERYCHANGECONFIG.</span><span class="sxs-lookup"><span data-stu-id="03d98-114">Set to DBT\_QUERYCHANGECONFIG.</span></span>

</dd> <dt>

<span data-ttu-id="03d98-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03d98-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03d98-116">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="03d98-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03d98-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="03d98-117">Return value</span></span>

<span data-ttu-id="03d98-118">Retorne **true** para conceder permissão para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="03d98-118">Return **TRUE** to grant permission to change the configuration.</span></span>

<span data-ttu-id="03d98-119">Retornar consulta de difusão \_ \_ negar para negar permissão para alterar a configuração.</span><span class="sxs-lookup"><span data-stu-id="03d98-119">Return BROADCAST\_QUERY\_DENY to deny permission to change the configuration.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d98-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03d98-120">Requirements</span></span>



| <span data-ttu-id="03d98-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="03d98-121">Requirement</span></span> | <span data-ttu-id="03d98-122">Valor</span><span class="sxs-lookup"><span data-stu-id="03d98-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="03d98-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d98-123">Minimum supported client</span></span><br/> | <span data-ttu-id="03d98-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="03d98-124">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="03d98-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03d98-125">Minimum supported server</span></span><br/> | <span data-ttu-id="03d98-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="03d98-126">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="03d98-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="03d98-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d98-128"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="03d98-128"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03d98-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="03d98-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d98-130">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="03d98-130">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="03d98-131">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="03d98-131">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="03d98-132">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="03d98-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




