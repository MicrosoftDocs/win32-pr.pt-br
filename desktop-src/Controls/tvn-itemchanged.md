---
title: TVN_ITEMCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que os atributos de item foram alterados. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b09164bc-54da-457a-9fb7-3beab3dae3e4
keywords:
- TVN_ITEMCHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGED
- TVN_ITEMCHANGEDA
- TVN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d58501d02cc2058ac803c949cc7118d7f146a10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824448"
---
# <a name="tvn_itemchanged-notification-code"></a><span data-ttu-id="cc934-105">Código de notificação TVN com \_ alterações</span><span class="sxs-lookup"><span data-stu-id="cc934-105">TVN\_ITEMCHANGED notification code</span></span>

<span data-ttu-id="cc934-106">Notifica uma janela pai do controle de exibição de árvore que os atributos de item foram alterados.</span><span class="sxs-lookup"><span data-stu-id="cc934-106">Notifies a tree-view control's parent window that item attributes have changed.</span></span> <span data-ttu-id="cc934-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="cc934-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGED
        
    pnm = (NMTVITEMCHANGE *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="cc934-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc934-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc934-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc934-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc934-110">Ponteiro para uma estrutura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que descreve o item que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="cc934-110">Pointer to a [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that changed.</span></span> <span data-ttu-id="cc934-111">O membro **uChanged** é definido como TVIF \_ State.</span><span class="sxs-lookup"><span data-stu-id="cc934-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc934-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc934-112">Return value</span></span>

<span data-ttu-id="cc934-113">Retorna **false** para aceitar a alteração ou **true** para evitar a alteração.</span><span class="sxs-lookup"><span data-stu-id="cc934-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc934-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc934-114">Requirements</span></span>



| <span data-ttu-id="cc934-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc934-115">Requirement</span></span> | <span data-ttu-id="cc934-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cc934-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc934-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc934-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc934-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc934-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cc934-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cc934-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc934-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc934-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc934-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc934-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc934-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc934-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cc934-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cc934-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cc934-124">**TVN \_ ITEMCHANGEDW** (Unicode) e **TVN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cc934-124">**TVN\_ITEMCHANGEDW** (Unicode) and **TVN\_ITEMCHANGEDA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="cc934-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc934-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc934-126">TVN de \_ alteração</span><span class="sxs-lookup"><span data-stu-id="cc934-126">TVN\_ITEMCHANGING</span></span>](tvn-itemchanging.md)
</dt> </dl>

 

 





