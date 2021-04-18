---
description: Evento de nível de sistema gerado em uma alteração de configuração de controles pais.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: WPCEVENT_SYS_SETTINGCHANGE evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771381"
---
# <a name="wpcevent_sys_settingchange-event"></a><span data-ttu-id="05ae4-103">\_Evento WPCEVENT sys \_ SETTINGCHANGE</span><span class="sxs-lookup"><span data-stu-id="05ae4-103">WPCEVENT\_SYS\_SETTINGCHANGE event</span></span>

<span data-ttu-id="05ae4-104">Evento de nível de sistema gerado em uma alteração de configuração de controles pais.</span><span class="sxs-lookup"><span data-stu-id="05ae4-104">System-level event generated on a Parental Controls setting change.</span></span>


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a><span data-ttu-id="05ae4-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05ae4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05ae4-106">*Classe*</span><span class="sxs-lookup"><span data-stu-id="05ae4-106">*Class*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-107">A classe que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="05ae4-107">The class that is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="05ae4-108">*Configuração*</span><span class="sxs-lookup"><span data-stu-id="05ae4-108">*Setting*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-109">Um valor da enumeração **de \_ configurações de WPC** .</span><span class="sxs-lookup"><span data-stu-id="05ae4-109">A value of the **WPC\_SETTINGS** enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="05ae4-110">*Proprietário*</span><span class="sxs-lookup"><span data-stu-id="05ae4-110">*Owner*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-111">O identificador de segurança do usuário que está gerando o evento.</span><span class="sxs-lookup"><span data-stu-id="05ae4-111">The security identifier of the user who is generating the event.</span></span>

</dd> <dt>

<span data-ttu-id="05ae4-112">*OldVal*</span><span class="sxs-lookup"><span data-stu-id="05ae4-112">*OldVal*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-113">O valor anterior dessa configuração, se excluído ou alterado.</span><span class="sxs-lookup"><span data-stu-id="05ae4-113">The previous value of this setting, if deleted or changed.</span></span>

</dd> <dt>

<span data-ttu-id="05ae4-114">*NewVal*</span><span class="sxs-lookup"><span data-stu-id="05ae4-114">*NewVal*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-115">O novo valor dessa configuração, se adicionado ou alterado.</span><span class="sxs-lookup"><span data-stu-id="05ae4-115">The new value of this setting, if added or changed.</span></span>

</dd> <dt>

<span data-ttu-id="05ae4-116">*Motivo*</span><span class="sxs-lookup"><span data-stu-id="05ae4-116">*Reason*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-117">Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.</span><span class="sxs-lookup"><span data-stu-id="05ae4-117">A value of the [**WPCFLAG\_ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) enumeration that indicates information about what events are blocked from use and what controls are in place.</span></span>

</dd> <dt>

<span data-ttu-id="05ae4-118">*Opcional*</span><span class="sxs-lookup"><span data-stu-id="05ae4-118">*Optional*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae4-119">Um campo opcional.</span><span class="sxs-lookup"><span data-stu-id="05ae4-119">An optional field.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="05ae4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05ae4-120">Requirements</span></span>



| <span data-ttu-id="05ae4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="05ae4-121">Requirement</span></span> | <span data-ttu-id="05ae4-122">Valor</span><span class="sxs-lookup"><span data-stu-id="05ae4-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05ae4-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05ae4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="05ae4-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05ae4-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05ae4-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05ae4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="05ae4-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="05ae4-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="05ae4-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="05ae4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="05ae4-128"><dt>Wpcevent. h</dt></span><span class="sxs-lookup"><span data-stu-id="05ae4-128"><dt>Wpcevent.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ae4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="05ae4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ae4-130">Usando APIs de log para controles dos pais</span><span class="sxs-lookup"><span data-stu-id="05ae4-130">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[<span data-ttu-id="05ae4-131">**WPC \_ args \_ CONVERSATIONINITEVENT**</span><span class="sxs-lookup"><span data-stu-id="05ae4-131">**WPC\_ARGS\_CONVERSATIONINITEVENT**</span></span>](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




