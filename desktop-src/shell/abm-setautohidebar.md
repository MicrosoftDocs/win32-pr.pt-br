---
description: Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela. Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.
title: Mensagem de ABM_SETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0cbd6c9c-e83f-41f8-91ed-81afaa24f524
api_name:
- ABM_SETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 53ca89008dda1233d12a7f0a9588803776ba1181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967375"
---
# <a name="abm_setautohidebar-message"></a><span data-ttu-id="23f25-104">\_Mensagem ABM SETAUTOHIDEBAR</span><span class="sxs-lookup"><span data-stu-id="23f25-104">ABM\_SETAUTOHIDEBAR message</span></span>

<span data-ttu-id="23f25-105">Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela.</span><span class="sxs-lookup"><span data-stu-id="23f25-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="23f25-106">Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.</span><span class="sxs-lookup"><span data-stu-id="23f25-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="23f25-107">Para registrar ou cancelar o registro de um AutoOcultar AppBar em um monitor específico, use [**ABM \_ SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="23f25-107">To register or unregister an autohide appbar on a specific monitor, use [**ABM\_SETAUTOHIDEBAREX**](abm-setautohidebarex.md).</span></span>

 


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="23f25-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23f25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23f25-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="23f25-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="23f25-110">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="23f25-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="23f25-111">Defina o membro **lParam** como **true** para registrar o AppBar ou **false** para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="23f25-111">Set the **lParam** member to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="23f25-112">Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **lParam** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="23f25-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23f25-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23f25-113">Return value</span></span>

<span data-ttu-id="23f25-114">Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro ou se um AutoOcultar AppBar já estiver registrado para a borda especificada.</span><span class="sxs-lookup"><span data-stu-id="23f25-114">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge.</span></span>

## <a name="remarks"></a><span data-ttu-id="23f25-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="23f25-115">Remarks</span></span>

<span data-ttu-id="23f25-116">O sistema permite apenas um AppBar de AutoOcultar para cada borda da tela.</span><span class="sxs-lookup"><span data-stu-id="23f25-116">The system allows only one autohide appbar for each edge of the screen.</span></span> <span data-ttu-id="23f25-117">Isso é determinado quando o membro **uEdge** da estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) é definido.</span><span class="sxs-lookup"><span data-stu-id="23f25-117">This is determined when the member **uEdge** of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="23f25-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23f25-118">Requirements</span></span>



| <span data-ttu-id="23f25-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="23f25-119">Requirement</span></span> | <span data-ttu-id="23f25-120">Valor</span><span class="sxs-lookup"><span data-stu-id="23f25-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23f25-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23f25-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23f25-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="23f25-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="23f25-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23f25-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23f25-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="23f25-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23f25-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="23f25-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="23f25-126"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="23f25-126"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23f25-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="23f25-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23f25-128">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="23f25-128">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="23f25-129">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="23f25-129">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="23f25-130">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="23f25-130">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




