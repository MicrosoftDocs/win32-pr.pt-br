---
description: Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela. Essa mensagem estende ABM \_ GETAUTOHIDEBAR permitindo que você especifique um monitor específico, para uso em várias situações de monitor.
title: Mensagem de ABM_GETAUTOHIDEBAREX (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 538EA230-06DF-4441-A6AA-9DD613521BE1
api_name:
- ABM_GETAUTOHIDEBAREX
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2ef95739a1031efb199e6acd99686e0858a9630e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104970801"
---
# <a name="abm_getautohidebarex-message"></a><span data-ttu-id="dbc1b-104">\_Mensagem ABM GETAUTOHIDEBAREX</span><span class="sxs-lookup"><span data-stu-id="dbc1b-104">ABM\_GETAUTOHIDEBAREX message</span></span>

<span data-ttu-id="dbc1b-105">Recupera o identificador para o AppBar de AutoOcultar associado a uma borda da tela.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-105">Retrieves the handle to the autohide appbar associated with an edge of the screen.</span></span> <span data-ttu-id="dbc1b-106">Essa mensagem estende [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) permitindo que você especifique um monitor específico, para uso em várias situações de monitor.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-106">This message extends [**ABM\_GETAUTOHIDEBAR**](abm-getautohidebar.md) by enabling you to specify a particular monitor, for use in multiple monitor situations.</span></span>


```C++
hwndAutoHide = (HWND) SHAppBarMessage(ABM_GETAUTOHIDEBAR, pabd);
```



## <a name="parameters"></a><span data-ttu-id="dbc1b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dbc1b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbc1b-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="dbc1b-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="dbc1b-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que especifica a borda e o monitor da tela.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that specifies the screen edge and monitor.</span></span> <span data-ttu-id="dbc1b-110">Você deve especificar os membros **cbSize**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-110">You must specify the **cbSize**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbc1b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dbc1b-111">Return value</span></span>

<span data-ttu-id="dbc1b-112">Retorna o identificador para o AutoOcultar AppBar.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-112">Returns the handle to the autohide appbar.</span></span> <span data-ttu-id="dbc1b-113">O valor de retorno será **nulo** se ocorrer um erro ou se nenhuma AppBar de AutoOcultar estiver associada à borda fornecida do monitor especificado.</span><span class="sxs-lookup"><span data-stu-id="dbc1b-113">The return value is **NULL** if an error occurs or if no autohide appbar is associated with the given edge of the given monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc1b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbc1b-114">Requirements</span></span>



| <span data-ttu-id="dbc1b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbc1b-115">Requirement</span></span> | <span data-ttu-id="dbc1b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="dbc1b-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbc1b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dbc1b-117">Header</span></span><br/> | <dl> <span data-ttu-id="dbc1b-118"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbc1b-118"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbc1b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbc1b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbc1b-120">**ABM \_ GETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="dbc1b-120">**ABM\_GETAUTOHIDEBAR**</span></span>](abm-getautohidebar.md)
</dt> <dt>

[<span data-ttu-id="dbc1b-121">**ABM \_ SETAUTOHIDEBAR**</span><span class="sxs-lookup"><span data-stu-id="dbc1b-121">**ABM\_SETAUTOHIDEBAR**</span></span>](abm-setautohidebar.md)
</dt> <dt>

[<span data-ttu-id="dbc1b-122">**ABM \_ SETAUTOHIDEBAREX**</span><span class="sxs-lookup"><span data-stu-id="dbc1b-122">**ABM\_SETAUTOHIDEBAREX**</span></span>](abm-setautohidebarex.md)
</dt> </dl>

 

 




