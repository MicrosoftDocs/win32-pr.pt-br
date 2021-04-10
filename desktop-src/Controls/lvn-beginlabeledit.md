---
title: LVN_BEGINLABELEDIT código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista sobre o início da edição de rótulo para um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f77550b474534cee096b610a0805bce547d9b429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918031"
---
# <a name="lvn_beginlabeledit-notification-code"></a><span data-ttu-id="90efd-105">Código de notificação do LVN \_ BEGINLABELEDIT</span><span class="sxs-lookup"><span data-stu-id="90efd-105">LVN\_BEGINLABELEDIT notification code</span></span>

<span data-ttu-id="90efd-106">Notifica uma janela pai do controle de exibição de lista sobre o início da edição de rótulo para um item.</span><span class="sxs-lookup"><span data-stu-id="90efd-106">Notifies a list-view control's parent window about the start of label editing for an item.</span></span> <span data-ttu-id="90efd-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="90efd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="90efd-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90efd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90efd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90efd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="90efd-110">Ponteiro para uma estrutura [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) .</span><span class="sxs-lookup"><span data-stu-id="90efd-110">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="90efd-111">O membro **Item** dessa estrutura é uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) cujo membro **iItem** identifica o item que está sendo editado.</span><span class="sxs-lookup"><span data-stu-id="90efd-111">The **item** member of this structure is an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure whose **iItem** member identifies the item being edited.</span></span> <span data-ttu-id="90efd-112">Observe que os subitens não podem ser editados; o membro **iSubItem** é sempre definido como zero.</span><span class="sxs-lookup"><span data-stu-id="90efd-112">Note that subitems cannot be edited; the **iSubItem** member is always set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90efd-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90efd-113">Return value</span></span>

<span data-ttu-id="90efd-114">Para permitir que o usuário edite o rótulo, retorne **false**.</span><span class="sxs-lookup"><span data-stu-id="90efd-114">To allow the user to edit the label, return **FALSE**.</span></span>

<span data-ttu-id="90efd-115">Para impedir que o usuário edite o rótulo, retorne **true**.</span><span class="sxs-lookup"><span data-stu-id="90efd-115">To prevent the user from editing the label, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="90efd-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="90efd-116">Remarks</span></span>

<span data-ttu-id="90efd-117">Quando o rótulo é iniciado, um controle de edição é criado, posicionado e inicializado.</span><span class="sxs-lookup"><span data-stu-id="90efd-117">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="90efd-118">Antes de ser exibida, o controle List-View envia à janela pai um \_ código de notificação LVN BEGINLABELEDIT.</span><span class="sxs-lookup"><span data-stu-id="90efd-118">Before it is displayed, the list-view control sends its parent window an LVN\_BEGINLABELEDIT notification code.</span></span>

<span data-ttu-id="90efd-119">Para personalizar a edição de rótulo, implemente um manipulador para LVN \_ BEGINLABELEDIT e envie uma mensagem de [**\_ GETEDITCONTROL LVM**](lvm-geteditcontrol.md) para o controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="90efd-119">To customize label editing, implement a handler for LVN\_BEGINLABELEDIT and have it send an [**LVM\_GETEDITCONTROL**](lvm-geteditcontrol.md) message to the list-view control.</span></span> <span data-ttu-id="90efd-120">Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="90efd-120">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="90efd-121">Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em **\_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="90efd-121">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="90efd-122">Quando o usuário cancela ou conclui a edição, a janela pai recebe um código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="90efd-122">When the user cancels or completes the editing, the parent window receives an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="90efd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90efd-123">Requirements</span></span>



| <span data-ttu-id="90efd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="90efd-124">Requirement</span></span> | <span data-ttu-id="90efd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="90efd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90efd-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90efd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="90efd-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90efd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90efd-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90efd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="90efd-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90efd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90efd-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90efd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="90efd-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90efd-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="90efd-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="90efd-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="90efd-133">**LVN \_ BEGINLABELEDITW** (Unicode) e **LVN \_ BEGINLABELEDITA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="90efd-133">**LVN\_BEGINLABELEDITW** (Unicode) and **LVN\_BEGINLABELEDITA** (ANSI)</span></span><br/>     |



 

 





