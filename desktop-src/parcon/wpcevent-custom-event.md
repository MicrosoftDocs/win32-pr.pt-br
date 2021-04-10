---
description: Evento por usuário que dá suporte a até três campos.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169357"
---
# <a name="wpcevent_custom-event"></a><span data-ttu-id="4cae1-103">\_Evento personalizado WPCEVENT</span><span class="sxs-lookup"><span data-stu-id="4cae1-103">WPCEVENT\_CUSTOM event</span></span>

<span data-ttu-id="4cae1-104">Evento por usuário que dá suporte a até três campos.</span><span class="sxs-lookup"><span data-stu-id="4cae1-104">Per-user event that supports up to three fields.</span></span>

<span data-ttu-id="4cae1-105">Os eventos são exibidos no **Visualizador de atividades** na **outra** seção com a seguinte hierarquia:</span><span class="sxs-lookup"><span data-stu-id="4cae1-105">Events are displayed in the **Activity Viewer** in the **Other** section with the following hierarchy:</span></span>

1.  <span data-ttu-id="4cae1-106">Publicador</span><span class="sxs-lookup"><span data-stu-id="4cae1-106">Publisher</span></span>

2.  <span data-ttu-id="4cae1-107">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4cae1-107">Application</span></span>

3.  <span data-ttu-id="4cae1-108">Evento</span><span class="sxs-lookup"><span data-stu-id="4cae1-108">Event</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a><span data-ttu-id="4cae1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4cae1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cae1-110">*Publicador*</span><span class="sxs-lookup"><span data-stu-id="4cae1-110">*Publisher*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-111">O editor do evento (por exemplo, um nome de empresa).</span><span class="sxs-lookup"><span data-stu-id="4cae1-111">The publisher of the event (for example, a company name).</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-112">*AppName*</span><span class="sxs-lookup"><span data-stu-id="4cae1-112">*AppName*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-113">O nome do aplicativo que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="4cae1-113">The name of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-114">*AppVersion*</span><span class="sxs-lookup"><span data-stu-id="4cae1-114">*AppVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-115">A versão do aplicativo que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="4cae1-115">The version of the application that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-116">*Evento*</span><span class="sxs-lookup"><span data-stu-id="4cae1-116">*Event*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-117">O nome do evento.</span><span class="sxs-lookup"><span data-stu-id="4cae1-117">The name for the event.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-118">*Value1*</span><span class="sxs-lookup"><span data-stu-id="4cae1-118">*Value1*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-119">Campo personalizado 1.</span><span class="sxs-lookup"><span data-stu-id="4cae1-119">Custom field 1.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-120">*Value2*</span><span class="sxs-lookup"><span data-stu-id="4cae1-120">*Value2*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-121">Campo personalizado 2.</span><span class="sxs-lookup"><span data-stu-id="4cae1-121">Custom field 2.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-122">*Value3*</span><span class="sxs-lookup"><span data-stu-id="4cae1-122">*Value3*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-123">Campo personalizado 3.</span><span class="sxs-lookup"><span data-stu-id="4cae1-123">Custom field 3.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-124">*Bloqueado*</span><span class="sxs-lookup"><span data-stu-id="4cae1-124">*Blocked*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-125">Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="4cae1-125">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="4cae1-126">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="4cae1-126">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="4cae1-127">Uma cadeia de caracteres personalizada que fornece informações adicionais sobre o motivo do bloqueio ou não do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="4cae1-127">A custom string that provides extra information about the reason for blocking or not blocking.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4cae1-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cae1-128">Requirements</span></span>



| <span data-ttu-id="4cae1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cae1-129">Requirement</span></span> | <span data-ttu-id="4cae1-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4cae1-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4cae1-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cae1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4cae1-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cae1-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4cae1-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cae1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4cae1-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4cae1-134">None supported</span></span><br/>                                                             |
| <span data-ttu-id="4cae1-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4cae1-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cae1-136"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cae1-136"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cae1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="4cae1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cae1-138">Usando APIs de log para controles dos pais</span><span class="sxs-lookup"><span data-stu-id="4cae1-138">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="4cae1-139">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="4cae1-139">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




