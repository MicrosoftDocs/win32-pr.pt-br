---
title: TVN_ITEMEXPANDED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a lista de itens filhos de um item pai foi expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086311"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="42f9a-105">\_Código de notificação TVN DOexpanded</span><span class="sxs-lookup"><span data-stu-id="42f9a-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="42f9a-106">Notifica uma janela pai do controle de exibição de árvore que a lista de itens filhos de um item pai foi expandida ou recolhida.</span><span class="sxs-lookup"><span data-stu-id="42f9a-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="42f9a-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="42f9a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="42f9a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42f9a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f9a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42f9a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42f9a-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="42f9a-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="42f9a-111">O membro **itemNew** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item pai nos membros **hItem**, **estado** e **lParam** .</span><span class="sxs-lookup"><span data-stu-id="42f9a-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="42f9a-112">O membro de **ação** indica se a lista foi expandida ou recolhida.</span><span class="sxs-lookup"><span data-stu-id="42f9a-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="42f9a-113">Para obter uma lista de valores possíveis, consulte a descrição da mensagem de [**\_ expansão TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="42f9a-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f9a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="42f9a-114">Return value</span></span>

<span data-ttu-id="42f9a-115">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="42f9a-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f9a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f9a-116">Requirements</span></span>



| <span data-ttu-id="42f9a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f9a-117">Requirement</span></span> | <span data-ttu-id="42f9a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="42f9a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42f9a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42f9a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42f9a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42f9a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42f9a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42f9a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42f9a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42f9a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42f9a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42f9a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42f9a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42f9a-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="42f9a-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="42f9a-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="42f9a-126">**TVN \_ ITEMEXPANDEDW** (Unicode) e **TVN \_** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="42f9a-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="42f9a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="42f9a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f9a-128">TVN ao \_ expandir</span><span class="sxs-lookup"><span data-stu-id="42f9a-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 





