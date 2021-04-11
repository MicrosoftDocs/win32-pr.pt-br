---
description: O \_ evento de dispositivo DBT USERdefined identifica um evento definido pelo usuário.
ms.assetid: b42feda9-5fe7-4e54-aad9-28c61d2f29b6
title: DBT_USERDEFINED evento (DBT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57ed3ebb801da4ae1ed7a7964cb7aac4f411a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010191"
---
# <a name="dbt_userdefined-event"></a><span data-ttu-id="54ebc-103">\_Evento DBT USERdefined</span><span class="sxs-lookup"><span data-stu-id="54ebc-103">DBT\_USERDEFINED event</span></span>

<span data-ttu-id="54ebc-104">O \_ evento de dispositivo DBT USERdefined identifica um evento definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54ebc-104">The DBT\_USERDEFINED device event identifies a user-defined event.</span></span>

<span data-ttu-id="54ebc-105">Para transmitir esse evento de dispositivo, chame a função [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) com a mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="54ebc-105">To broadcast this device event, call the [**BroadcastSystemMessage**](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage) function with the [**WM\_DEVICECHANGE**](wm-devicechange.md) message.</span></span> <span data-ttu-id="54ebc-106">Defina *wParam* como DBT UserDefined \_ e defina *lParam* conforme descrito a seguir.</span><span class="sxs-lookup"><span data-stu-id="54ebc-106">Set *wParam* to DBT\_USERDEFINED and set *lParam* as described following.</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND   hwnd,     // handle to window
                             UINT   uMsg,     // WM_DEVICECHANGE
                             WPARAM wParam,   // DBT_USERDEFINED
                             LPARAM lParam ); // event-specific data
```



## <a name="parameters"></a><span data-ttu-id="54ebc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="54ebc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54ebc-108">*HWND*</span><span class="sxs-lookup"><span data-stu-id="54ebc-108">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="54ebc-109">Um identificador para uma janela.</span><span class="sxs-lookup"><span data-stu-id="54ebc-109">A handle to a window.</span></span>

</dd> <dt>

<span data-ttu-id="54ebc-110">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="54ebc-110">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="54ebc-111">O identificador de mensagem do [**WM \_ DEVICECHANGE**](wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="54ebc-111">The [**WM\_DEVICECHANGE**](wm-devicechange.md) message identifier.</span></span>

</dd> <dt>

<span data-ttu-id="54ebc-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54ebc-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54ebc-113">Defina como DBT \_ USERdefined.</span><span class="sxs-lookup"><span data-stu-id="54ebc-113">Set to DBT\_USERDEFINED.</span></span>

</dd> <dt>

<span data-ttu-id="54ebc-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54ebc-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54ebc-115">Um ponteiro para uma estrutura [**\_ \_ \_ userdefineda de difusão de desenvolvimento**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) que descreve a difusão definida pelo usuário em andamento.</span><span class="sxs-lookup"><span data-stu-id="54ebc-115">A pointer to a [**\_DEV\_BROADCAST\_USERDEFINED**](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined) structure which describes the user-defined broadcast in progress.</span></span> <span data-ttu-id="54ebc-116">O membro **dbud \_ szName** contém o nome da mensagem definida pelo usuário, seguido por qualquer dado definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="54ebc-116">The **dbud\_szName** member contains the name of the user-defined message, followed by any user-defined data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54ebc-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="54ebc-117">Return value</span></span>

<span data-ttu-id="54ebc-118">Retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="54ebc-118">Return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="54ebc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54ebc-119">Requirements</span></span>



| <span data-ttu-id="54ebc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="54ebc-120">Requirement</span></span> | <span data-ttu-id="54ebc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="54ebc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="54ebc-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54ebc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54ebc-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="54ebc-123">Windows XP</span></span><br/>                                                            |
| <span data-ttu-id="54ebc-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54ebc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54ebc-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="54ebc-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="54ebc-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54ebc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54ebc-127"><dt>DBT. h</dt></span><span class="sxs-lookup"><span data-stu-id="54ebc-127"><dt>Dbt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54ebc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="54ebc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54ebc-129">Eventos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="54ebc-129">Device Events</span></span>](device-events.md)
</dt> <dt>

[<span data-ttu-id="54ebc-130">Eventos de gerenciamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="54ebc-130">Device Management Events</span></span>](device-management-events.md)
</dt> <dt>

[<span data-ttu-id="54ebc-131">**\_UserDefined de difusão de DEV \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54ebc-131">**\_DEV\_BROADCAST\_USERDEFINED**</span></span>](/windows/win32/api/dbt/ns-dbt-_dev_broadcast_userdefined)
</dt> <dt>

[<span data-ttu-id="54ebc-132">**DEVICECHANGE do WM \_**</span><span class="sxs-lookup"><span data-stu-id="54ebc-132">**WM\_DEVICECHANGE**</span></span>](wm-devicechange.md)
</dt> <dt>

[<span data-ttu-id="54ebc-133">**BroadcastSystemMessage**</span><span class="sxs-lookup"><span data-stu-id="54ebc-133">**BroadcastSystemMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-broadcastsystemmessage)
</dt> </dl>

 

