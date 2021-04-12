---
title: TVN_ITEMCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que os atributos de item estão prestes a serem alterados. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499390"
---
# <a name="tvn_itemchanging-notification-code"></a><span data-ttu-id="5824e-105">Código de notificação de TVN de \_ alteração</span><span class="sxs-lookup"><span data-stu-id="5824e-105">TVN\_ITEMCHANGING notification code</span></span>

<span data-ttu-id="5824e-106">Notifica uma janela pai do controle de exibição de árvore que os atributos de item estão prestes a serem alterados.</span><span class="sxs-lookup"><span data-stu-id="5824e-106">Notifies a tree-view control's parent window that item attributes are about to change.</span></span> <span data-ttu-id="5824e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5824e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5824e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5824e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5824e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5824e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5824e-110">Ponteiro para uma estrutura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que descreve o item que está sendo alterado.</span><span class="sxs-lookup"><span data-stu-id="5824e-110">Pointer to an [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) structure describing the item that is changing.</span></span> <span data-ttu-id="5824e-111">O membro **uChanged** é definido como TVIF \_ State.</span><span class="sxs-lookup"><span data-stu-id="5824e-111">The **uChanged** member is set to TVIF\_STATE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5824e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5824e-112">Return value</span></span>

<span data-ttu-id="5824e-113">Retorna **false** para aceitar a alteração ou **true** para evitar a alteração.</span><span class="sxs-lookup"><span data-stu-id="5824e-113">Returns **FALSE** to accept the change, or **TRUE** to prevent the change.</span></span>

## <a name="requirements"></a><span data-ttu-id="5824e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5824e-114">Requirements</span></span>



| <span data-ttu-id="5824e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5824e-115">Requirement</span></span> | <span data-ttu-id="5824e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5824e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5824e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5824e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5824e-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5824e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5824e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5824e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5824e-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5824e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5824e-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5824e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="5824e-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5824e-122"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="5824e-123">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="5824e-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5824e-124">**TVN \_ ITEMCHANGINGW** (Unicode) e **TVN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5824e-124">**TVN\_ITEMCHANGINGW** (Unicode) and **TVN\_ITEMCHANGINGA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="5824e-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5824e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5824e-126">TVN \_ PERalterados</span><span class="sxs-lookup"><span data-stu-id="5824e-126">TVN\_ITEMCHANGED</span></span>](tvn-itemchanged.md)
</dt> </dl>

 

 





