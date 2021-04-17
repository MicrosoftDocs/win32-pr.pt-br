---
title: TVN_BEGINLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34eccdeda553d0792a2862e3ca81a0889539d5ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750933"
---
# <a name="tvn_beginlabeledit-notification-code"></a><span data-ttu-id="7af67-105">Código de notificação do TVN \_ BEGINLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="7af67-105">TVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="7af67-106">Notifica uma janela pai do controle de exibição de árvore sobre o início da edição de rótulo para um item.</span><span class="sxs-lookup"><span data-stu-id="7af67-106">Notifies a tree-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="7af67-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7af67-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a><span data-ttu-id="7af67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7af67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af67-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7af67-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7af67-110">Ponteiro para uma estrutura [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="7af67-110">Pointer to an [**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa) structure.</span></span> <span data-ttu-id="7af67-111">O membro **Item** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item que está sendo editado nos membros **hItem**, **State**, **lParam** e **pszText** .</span><span class="sxs-lookup"><span data-stu-id="7af67-111">The **item** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the item being edited in the **hItem**, **state**, **lParam**, and **pszText** members.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af67-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7af67-112">Return value</span></span>

<span data-ttu-id="7af67-113">Retorna **true** para cancelar a edição do rótulo.</span><span class="sxs-lookup"><span data-stu-id="7af67-113">Returns **TRUE** to cancel label editing.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af67-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="7af67-114">Remarks</span></span>

<span data-ttu-id="7af67-115">Quando o rótulo é iniciado, um controle de edição é criado, mas não posicionado ou exibido.</span><span class="sxs-lookup"><span data-stu-id="7af67-115">When label editing begins, an edit control is created but not positioned or displayed.</span></span> <span data-ttu-id="7af67-116">Antes de ser exibida, o controle de exibição de árvore envia a janela pai um \_ código de notificação TVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="7af67-116">Before it is displayed, the tree-view control sends its parent window a TVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="7af67-117">Para personalizar a edição de rótulo, implemente um manipulador para TVN \_ BEGINLABELEDIT e envie uma mensagem [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) para o controle de exibição em árvore.</span><span class="sxs-lookup"><span data-stu-id="7af67-117">To customize label editing, implement a handler for TVN\_BEGINLABELEDIT and have it send a [**TVM\_GETEDITCONTROL**](tvm-geteditcontrol.md) message to the tree-view control.</span></span> <span data-ttu-id="7af67-118">Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="7af67-118">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="7af67-119">Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em \_ xxx.</span><span class="sxs-lookup"><span data-stu-id="7af67-119">Use this handle to customize the edit control by sending the usual EM\_XXX messages.</span></span>

<span data-ttu-id="7af67-120">Quando o usuário cancela ou conclui a edição, a janela pai recebe um código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="7af67-120">When the user cancels or completes the editing, the parent window receives a [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af67-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7af67-121">Requirements</span></span>



| <span data-ttu-id="7af67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af67-122">Requirement</span></span> | <span data-ttu-id="7af67-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7af67-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7af67-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7af67-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7af67-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7af67-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7af67-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7af67-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7af67-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7af67-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7af67-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7af67-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7af67-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7af67-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7af67-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7af67-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7af67-131">**TVN \_ BEGINLABELEDITW** (Unicode) e **TVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7af67-131">**TVN\_BEGINLABELEDITW** (Unicode) and **TVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





