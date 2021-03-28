---
description: Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela. Essa mensagem estende ABM \_ SETAUTOHIDEBAR permitindo que você especifique um monitor específico, para uso em várias situações de monitor.
title: Mensagem de ABM_SETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C437727C-3FF6-4598-9D81-A39FCC2EF1C4
api_name:
- ABM_SETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ba4e1474d3b57465fa68446fd7ab787c9a62570b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104989462"
---
# <a name="abm_setautohidebarex-message"></a><span data-ttu-id="5d4de-104">\_Mensagem ABM SETAUTOHIDEBAREX</span><span class="sxs-lookup"><span data-stu-id="5d4de-104">ABM\_SETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="5d4de-105">Registra ou cancela o registro de um AutoOcultar AppBar para uma determinada borda da tela.</span><span class="sxs-lookup"><span data-stu-id="5d4de-105">Registers or unregisters an autohide appbar for a given edge of the screen.</span></span> <span data-ttu-id="5d4de-106">Essa mensagem estende [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) permitindo que você especifique um monitor específico, para uso em várias situações de monitor.</span><span class="sxs-lookup"><span data-stu-id="5d4de-106">This message extends [**ABM\_SETAUTOHIDEBAR**](abm-setautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
fSuccess = (BOOL) SHAppBarMessage(ABM_SETAUTOHIDEBAR, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="5d4de-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d4de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d4de-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="5d4de-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="5d4de-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="5d4de-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="5d4de-110">Defina o membro **lParam** como **true** para registrar AppBar ou **false** para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="5d4de-110">Set the **lParam** member is to **TRUE** to register the appbar or **FALSE** to unregister it.</span></span> <span data-ttu-id="5d4de-111">Você deve especificar os membros **cbSize**, **HWND**, **uEdge**, **RC** e **lParam** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="5d4de-111">You must specify the **cbSize**, **hWnd**, **uEdge**, **rc**, and **lParam** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d4de-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d4de-112">Return value</span></span>

<span data-ttu-id="5d4de-113">Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro ou se um AutoOcultar AppBar já estiver registrado para a borda especificada no monitor especificado.</span><span class="sxs-lookup"><span data-stu-id="5d4de-113">Returns **TRUE** if successful, or **FALSE** if an error occurs or if an autohide appbar is already registered for the given edge on the given monitor.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4de-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d4de-114">Remarks</span></span>

<span data-ttu-id="5d4de-115">O sistema permite apenas um AppBar de AutoOcultar para cada borda de cada monitor.</span><span class="sxs-lookup"><span data-stu-id="5d4de-115">The system allows only one autohide appbar for each edge of each monitor.</span></span> <span data-ttu-id="5d4de-116">O monitor é determinado pelo membro **RC** e a borda é determinada pelo membro **UEdge** da estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="5d4de-116">The monitor is determined by the **rc** member and the edge is determined by the **uEdge** member of the [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d4de-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d4de-117">Requirements</span></span>



| <span data-ttu-id="5d4de-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d4de-118">Requirement</span></span> | <span data-ttu-id="5d4de-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5d4de-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d4de-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d4de-120">Header</span></span><br/> | <dl> <span data-ttu-id="5d4de-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d4de-121"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d4de-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d4de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d4de-123">**ABM \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="5d4de-123">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="5d4de-124">**ABM \_ GETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="5d4de-124">**ABM\_GETAUTOHIDEBAREX**</span></span>](abm-getautohidebarex.md)
</dt> <dt>

[<span data-ttu-id="5d4de-125">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="5d4de-125">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> </dl>

 

 




