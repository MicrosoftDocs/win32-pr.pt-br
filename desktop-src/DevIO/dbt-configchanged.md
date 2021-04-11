---
description: O sistema transmite o evento de \_ dispositivo DBT ConfigChanged para indicar que a configuração atual foi alterada, devido a um encaixe ou desencaixe. Um aplicativo ou driver que armazena dados no registro sob a chave de \_ configuração atual do hKey \_ deve atualizar os dados.
ms.assetid: e5e33970-b17e-4723-98aa-e242f90fe4e7
title: DBT_CONFIGCHANGED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242832378ba9ca3d3006965719942aa41ecff93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164029"
---
# <a name="dbt_configchanged-event"></a><span data-ttu-id="2e1e0-104">\_Evento DBT ConfigChanged</span><span class="sxs-lookup"><span data-stu-id="2e1e0-104">DBT\_CONFIGCHANGED event</span></span>

<span data-ttu-id="2e1e0-105">O sistema transmite o evento de \_ dispositivo DBT ConfigChanged para indicar que a configuração atual foi alterada, devido a um encaixe ou desencaixe.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-105">The system broadcasts the DBT\_CONFIGCHANGED device event to indicate that the current configuration has changed, due to a dock or undock.</span></span> <span data-ttu-id="2e1e0-106">Um aplicativo ou driver que armazena dados no registro sob a chave de \_ configuração atual do hKey \_ deve atualizar os dados.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-106">An application or driver that stores data in the registry under the HKEY\_CURRENT\_CONFIG key should update the data.</span></span>

<span data-ttu-id="2e1e0-107">Para transmitir esse evento de dispositivo, o sistema usa a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) com *wParam* definido como DBT \_ ConfigChanged e *lParam* definido como zero.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-107">To broadcast this device event, the system uses the [**WM\_DEVICECHANGE**](wm-devicechange.md) message with *wParam* set to DBT\_CONFIGCHANGED and *lParam* set to zero.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd,       // handle to window
  UINT uMsg,       // WM_DEVICECHANGE
  WPARAM wParam,   // device-change event
  LPARAM lParam    // event-specific data
);
```



## <a name="parameters"></a><span data-ttu-id="2e1e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e1e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e1e0-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="2e1e0-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="2e1e0-110">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-110">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="2e1e0-111">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="2e1e0-111">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="2e1e0-112">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="2e1e0-112">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2e1e0-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2e1e0-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e1e0-114">Defina como DBT \_ ConfigChanged.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-114">Set to DBT\_CONFIGCHANGED.</span></span>

</dd> <dt>

<span data-ttu-id="2e1e0-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2e1e0-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2e1e0-116">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-116">Set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e1e0-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2e1e0-117">Return value</span></span>

<span data-ttu-id="2e1e0-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="2e1e0-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e1e0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e1e0-119">Requirements</span></span>



| <span data-ttu-id="2e1e0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e1e0-120">Requirement</span></span> | <span data-ttu-id="2e1e0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2e1e0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e1e0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e1e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2e1e0-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e1e0-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="2e1e0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e1e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2e1e0-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2e1e0-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="2e1e0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e1e0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e1e0-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e1e0-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e1e0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e1e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e1e0-129">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2e1e0-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="2e1e0-130">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="2e1e0-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="2e1e0-131">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="2e1e0-131">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> </dl>

 

 




