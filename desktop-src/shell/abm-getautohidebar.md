---
description: Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela. Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.
title: Mensagem de ABM_GETAUTOHIDEBAR (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 545dd1d9-8cbb-4ff3-b871-4908ecac56db
api_name:
- ABM_GETAUTOHIDEBAR
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 979825a9dbc28a89e3579419542877faacbace45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090036"
---
# <a name="abm_getautohidebar-message"></a><span data-ttu-id="c5871-104">\_Mensagem ABM GETAUTOHIDEBAR</span><span class="sxs-lookup"><span data-stu-id="c5871-104">ABM\_GETAUTOHIDEBAR message</span></span>

<span data-ttu-id="c5871-105">Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela.</span><span class="sxs-lookup"><span data-stu-id="c5871-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="c5871-106">Se o sistema tiver vários monitores, o monitor que contém a barra de tarefas principal será usado.</span><span class="sxs-lookup"><span data-stu-id="c5871-106">If the system has multiple monitors, the monitor that contains the primary taskbar is used.</span></span>

> [!Note]  
> <span data-ttu-id="c5871-107">Para consultar uma AutoOcultar AppBar em um monitor específico, use [**ABM \_ GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span><span class="sxs-lookup"><span data-stu-id="c5871-107">To query for an autohide appbar on a specific monitor, use [**ABM\_GETAUTOHIDEBAREX**](abm-getautohidebarex.md).</span></span>

 


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="c5871-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5871-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5871-109">*pabd*</span><span class="sxs-lookup"><span data-stu-id="c5871-109">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c5871-110">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica a borda da tela.</span><span class="sxs-lookup"><span data-stu-id="c5871-110">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge.</span></span> <span data-ttu-id="c5871-111">Você deve especificar os membros **cbSize** e **uEdge** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="c5871-111">You must specify the **cbSize** and **uEdge** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5871-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5871-112">Return value</span></span>

<span data-ttu-id="c5871-113">Retorna o identificador para o AutoOcultar AppBar.</span><span class="sxs-lookup"><span data-stu-id="c5871-113">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="c5871-114">O valor de retorno será **nulo** se ocorrer um erro ou se nenhuma AppBar de AutoOcultar estiver associada à borda especificada.</span><span class="sxs-lookup"><span data-stu-id="c5871-114">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5871-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5871-115">Requirements</span></span>



| <span data-ttu-id="c5871-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5871-116">Requirement</span></span> | <span data-ttu-id="c5871-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c5871-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5871-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5871-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c5871-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c5871-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c5871-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5871-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c5871-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5871-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5871-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c5871-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5871-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5871-123"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5871-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5871-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5871-125">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="c5871-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="c5871-126">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="c5871-126">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="c5871-127">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="c5871-127">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




