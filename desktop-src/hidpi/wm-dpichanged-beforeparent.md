---
title: Mensagem de WM_DPICHANGED_BEFOREPARENT (WinUser. h)
description: Para as janelas de nível superior de cada monitor v2, essa mensagem é enviada a todos os HWNDs na árvore HWDN filho da janela que está passando por uma alteração de DPI. | Mensagem de WM_DPICHANGED_BEFOREPARENT (WinUser. h)
ms.assetid: EC8CC313-565F-451F-AE18-66F3B63303CE
keywords:
- DPI alta de mensagem de WM_DPICHANGED_BEFOREPARENT
topic_type:
- apiref
api_name:
- WM_DPICHANGED_BEFOREPARENT
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16641916cb16b789f2349a53b09dbd2af5f520f3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930496"
---
# <a name="wm_dpichanged_beforeparent-message"></a><span data-ttu-id="93315-105">Mensagem de BEFOREPARENT do WM \_ DPICHANGED \_</span><span class="sxs-lookup"><span data-stu-id="93315-105">WM\_DPICHANGED\_BEFOREPARENT message</span></span>

<span data-ttu-id="93315-106">Para as janelas de nível superior de [cada monitor v2](dpi-awareness-context.md) , essa mensagem é enviada a todos os HWNDs na árvore HWDN filho da janela que está passando por uma alteração de DPI.</span><span class="sxs-lookup"><span data-stu-id="93315-106">For [Per Monitor v2](dpi-awareness-context.md) top-level windows, this message is sent to all HWNDs in the child HWDN tree of the window that is undergoing a DPI change.</span></span> <span data-ttu-id="93315-107">Essa mensagem ocorre antes que a janela de nível superior receba o [**WM \_ DPICHANGED**](wm-dpichanged.md)e percorra a árvore filho de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="93315-107">This message occurs before the top-level window receives [**WM\_DPICHANGED**](wm-dpichanged.md), and traverses the child tree from the bottom up.</span></span>


```C++
#define WM_DPICHANGED_BEFOREPARENT       0x02E2
```



## <a name="parameters"></a><span data-ttu-id="93315-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="93315-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93315-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="93315-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93315-110">Esse valor não é usado e será zero.</span><span class="sxs-lookup"><span data-stu-id="93315-110">This value is unused and will be zero.</span></span>

</dd> <dt>

<span data-ttu-id="93315-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="93315-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="93315-112">Esse valor não é usado e será zero.</span><span class="sxs-lookup"><span data-stu-id="93315-112">This value is unused and will be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93315-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="93315-113">Return value</span></span>

<span data-ttu-id="93315-114">Esse valor não é usado e ignorado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="93315-114">This value is unused and ignored by the system.</span></span>

## <a name="remarks"></a><span data-ttu-id="93315-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="93315-115">Remarks</span></span>

<span data-ttu-id="93315-116">Não há nenhum tratamento padrão dessa mensagem no [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="93315-116">There is no default handling of this message in [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="93315-117">Essa mensagem é enviada somente quando a janela de nível superior tem um contexto de reconhecimento de DPI de PMv2.</span><span class="sxs-lookup"><span data-stu-id="93315-117">This message is only sent when the top-level window has a DPI awareness context of PMv2.</span></span>

## <a name="requirements"></a><span data-ttu-id="93315-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93315-118">Requirements</span></span>



| <span data-ttu-id="93315-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="93315-119">Requirement</span></span> | <span data-ttu-id="93315-120">Valor</span><span class="sxs-lookup"><span data-stu-id="93315-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93315-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93315-121">Minimum supported client</span></span><br/> | <span data-ttu-id="93315-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="93315-122">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="93315-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93315-123">Minimum supported server</span></span><br/> | <span data-ttu-id="93315-124">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="93315-124">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="93315-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="93315-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="93315-126"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="93315-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93315-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="93315-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93315-128">**DPICHANGED do WM \_**</span><span class="sxs-lookup"><span data-stu-id="93315-128">**WM\_DPICHANGED**</span></span>](wm-dpichanged.md)
</dt> <dt>

[<span data-ttu-id="93315-129">**AFTERPARENT do WM \_ DPICHANGED \_**</span><span class="sxs-lookup"><span data-stu-id="93315-129">**WM\_DPICHANGED\_AFTERPARENT**</span></span>](wm-dpichanged-afterparent.md)
</dt> </dl>

 

