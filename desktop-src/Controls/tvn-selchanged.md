---
title: TVN_SELCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a seleção foi alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824745"
---
# <a name="tvn_selchanged-notification-code"></a><span data-ttu-id="79860-105">Código de notificação do TVN \_ SELCHANGED</span><span class="sxs-lookup"><span data-stu-id="79860-105">TVN\_SELCHANGED notification code</span></span>

<span data-ttu-id="79860-106">Notifica uma janela pai do controle de exibição de árvore que a seleção foi alterada de um item para outro.</span><span class="sxs-lookup"><span data-stu-id="79860-106">Notifies a tree-view control's parent window that the selection has changed from one item to another.</span></span> <span data-ttu-id="79860-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="79860-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="79860-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79860-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79860-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79860-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="79860-110">Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="79860-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="79860-111">Os membros **itemOld** e **ItemNew** da estrutura **NMTREEVIEW** são estruturas [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contêm informações sobre o item selecionado anteriormente e o item recentemente selecionado.</span><span class="sxs-lookup"><span data-stu-id="79860-111">The **itemOld** and **itemNew** members of the **NMTREEVIEW** structure are [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structures that contain information about the previously selected item and the newly selected item.</span></span> <span data-ttu-id="79860-112">Somente os membros **máscara**, **hItem**, **estado** e **lParam** dessas estruturas são válidos.</span><span class="sxs-lookup"><span data-stu-id="79860-112">Only the **mask**, **hItem**, **state**, and **lParam** members of these structures are valid.</span></span> <span data-ttu-id="79860-113">Os membros **stateMask** das estruturas **TVITEM** especificadas por **itemOld** e **itemNew** são indefinidos na entrada.</span><span class="sxs-lookup"><span data-stu-id="79860-113">The **stateMask** members of the **TVITEM** structures specified by **itemOld** and **itemNew** are undefined on input.</span></span> <span data-ttu-id="79860-114">O membro **Action** da estrutura **NMTREEVIEW** indica o tipo de ação que causou a alteração da seleção.</span><span class="sxs-lookup"><span data-stu-id="79860-114">The **action** member of the **NMTREEVIEW** structure indicates the type of action that caused the selection to change.</span></span> <span data-ttu-id="79860-115">Pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="79860-115">It can be one of the following values:</span></span>



| <span data-ttu-id="79860-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79860-116">Requirement</span></span> | <span data-ttu-id="79860-117">Valor</span><span class="sxs-lookup"><span data-stu-id="79860-117">Value</span></span> |
|-----------------|-------------------|
| <span data-ttu-id="79860-118">TVC \_ BYKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="79860-118">TVC\_BYKEYBOARD</span></span> | <span data-ttu-id="79860-119">Por um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="79860-119">By a keystroke.</span></span>   |
| <span data-ttu-id="79860-120">TVC \_ BYMOUSE</span><span class="sxs-lookup"><span data-stu-id="79860-120">TVC\_BYMOUSE</span></span>    | <span data-ttu-id="79860-121">Com um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="79860-121">By a mouse click.</span></span> |
| <span data-ttu-id="79860-122">TVC \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="79860-122">TVC\_UNKNOWN</span></span>    | <span data-ttu-id="79860-123">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="79860-123">Unknown.</span></span>          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79860-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79860-124">Return value</span></span>

<span data-ttu-id="79860-125">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="79860-125">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="79860-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79860-126">Requirements</span></span>



| <span data-ttu-id="79860-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="79860-127">Requirement</span></span> | <span data-ttu-id="79860-128">Valor</span><span class="sxs-lookup"><span data-stu-id="79860-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79860-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79860-129">Minimum supported client</span></span><br/> | <span data-ttu-id="79860-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79860-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79860-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79860-131">Minimum supported server</span></span><br/> | <span data-ttu-id="79860-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79860-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79860-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79860-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="79860-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79860-134"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="79860-135">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="79860-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="79860-136">**TVN \_ SELCHANGEDW** (Unicode) e **TVN \_ SELCHANGEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="79860-136">**TVN\_SELCHANGEDW** (Unicode) and **TVN\_SELCHANGEDA** (ANSI)</span></span><br/>             |



 

 





