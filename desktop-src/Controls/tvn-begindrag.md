---
title: TVN_BEGINDRAG código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que uma operação de arrastar e soltar que envolve o botão esquerdo do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e118354a-329e-424c-b137-78342cc00957
keywords:
- TVN_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_BEGINDRAG
- TVN_BEGINDRAGA
- TVN_BEGINDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f47f55a5e2eae552f64234a8e43ef0961f38c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824449"
---
# <a name="tvn_begindrag-notification-code"></a><span data-ttu-id="f369f-105">Código de notificação do TVN \_ BEGINDRAG</span><span class="sxs-lookup"><span data-stu-id="f369f-105">TVN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="f369f-106">Notifica uma janela pai do controle de exibição de árvore que uma operação de arrastar e soltar que envolve o botão esquerdo do mouse está sendo iniciada.</span><span class="sxs-lookup"><span data-stu-id="f369f-106">Notifies a tree-view control's parent window that a drag-and-drop operation involving the left mouse button is being initiated.</span></span> <span data-ttu-id="f369f-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f369f-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="f369f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f369f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f369f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f369f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f369f-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="f369f-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="f369f-111">O membro **itemNew** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item que está sendo arrastado nos membros **hItem**, **estado** e **lParam** .</span><span class="sxs-lookup"><span data-stu-id="f369f-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being dragged in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="f369f-112">O membro **ptDrag** especifica as coordenadas de tela atuais do mouse.</span><span class="sxs-lookup"><span data-stu-id="f369f-112">The **ptDrag** member specifies the current screen coordinates of the mouse.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f369f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f369f-113">Return value</span></span>

<span data-ttu-id="f369f-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f369f-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f369f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f369f-115">Remarks</span></span>

<span data-ttu-id="f369f-116">Um controle de exibição de árvore que tem o estilo [**\_ DISABLEDRAGDROP de TVs**](tree-view-control-window-styles.md) não envia esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="f369f-116">A tree-view control that has the [**TVS\_DISABLEDRAGDROP**](tree-view-control-window-styles.md) style does not send this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f369f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f369f-117">Requirements</span></span>



| <span data-ttu-id="f369f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f369f-118">Requirement</span></span> | <span data-ttu-id="f369f-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f369f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f369f-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f369f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f369f-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f369f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f369f-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f369f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f369f-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f369f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f369f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f369f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f369f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f369f-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f369f-126">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f369f-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f369f-127">**TVN \_ BEGINDRAGW** (Unicode) e **TVN \_ BEGINDRAGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f369f-127">**TVN\_BEGINDRAGW** (Unicode) and **TVN\_BEGINDRAGA** (ANSI)</span></span><br/>               |



 

 





