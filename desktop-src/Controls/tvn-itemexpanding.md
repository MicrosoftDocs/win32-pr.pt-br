---
title: TVN_ITEMEXPANDING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a lista de itens filho de um item pai está prestes a ser expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919072"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="136b7-105">Código de notificação do TVN- \_ Expanding</span><span class="sxs-lookup"><span data-stu-id="136b7-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="136b7-106">Notifica uma janela pai do controle de exibição de árvore que a lista de itens filho de um item pai está prestes a ser expandida ou recolhida.</span><span class="sxs-lookup"><span data-stu-id="136b7-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="136b7-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="136b7-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="136b7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="136b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="136b7-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="136b7-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="136b7-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="136b7-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="136b7-111">O membro **itemNew** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item pai nos membros **hItem**, **estado** e **lParam** .</span><span class="sxs-lookup"><span data-stu-id="136b7-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="136b7-112">O membro de **ação** indica se a lista deve ser expandida ou recolhida.</span><span class="sxs-lookup"><span data-stu-id="136b7-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="136b7-113">Para obter uma lista de valores possíveis, consulte a descrição da mensagem de [**\_ expansão TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="136b7-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="136b7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="136b7-114">Return value</span></span>

<span data-ttu-id="136b7-115">Retorna **true** para impedir que a lista expanda ou recolha.</span><span class="sxs-lookup"><span data-stu-id="136b7-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="136b7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="136b7-116">Requirements</span></span>



| <span data-ttu-id="136b7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="136b7-117">Requirement</span></span> | <span data-ttu-id="136b7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="136b7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="136b7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="136b7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="136b7-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="136b7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="136b7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="136b7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="136b7-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="136b7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="136b7-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="136b7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="136b7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="136b7-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="136b7-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="136b7-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="136b7-126">**TVN \_ ITEMEXPANDINGW** (Unicode) e **TVN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="136b7-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="136b7-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="136b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136b7-128">TVN \_ DOexpanded</span><span class="sxs-lookup"><span data-stu-id="136b7-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 





