---
title: Mensagem de LVM_EDITLABEL (commctrl. h)
description: Inicia a edição in-loco do texto do item de exibição de lista especificado. A mensagem seleciona implicitamente e concentra o item especificado. Você pode enviar essa mensagem explicitamente ou usando a \_ macro EditLabel do ListView.
ms.assetid: b63f13f1-6e66-4770-af84-30bcdb241727
keywords:
- Controles de LVM_EDITLABEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_EDITLABEL
- LVM_EDITLABELA
- LVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25cb4e119731c41130e1c19fdea2f74882796435
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644266"
---
# <a name="lvm_editlabel-message"></a><span data-ttu-id="cb620-106">\_Mensagem EDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="cb620-106">LVM\_EDITLABEL message</span></span>

<span data-ttu-id="cb620-107">Inicia a edição in-loco do texto do item de exibição de lista especificado.</span><span class="sxs-lookup"><span data-stu-id="cb620-107">Begins in-place editing of the specified list-view item's text.</span></span> <span data-ttu-id="cb620-108">A mensagem seleciona implicitamente e concentra o item especificado.</span><span class="sxs-lookup"><span data-stu-id="cb620-108">The message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="cb620-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ EditLabel do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="cb620-109">You can send this message explicitly or by using the [**ListView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-listview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb620-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb620-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb620-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb620-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb620-112">O índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="cb620-112">The index of the list-view item.</span></span> <span data-ttu-id="cb620-113">Para cancelar a edição, defina o índice como-1.</span><span class="sxs-lookup"><span data-stu-id="cb620-113">To cancel editing, set the index to -1.</span></span>

</dd> <dt>

<span data-ttu-id="cb620-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb620-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cb620-115">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cb620-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb620-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cb620-116">Return value</span></span>

<span data-ttu-id="cb620-117">Retorna o identificador para o controle de edição que é usado para editar o texto do item, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cb620-117">Returns the handle to the edit control that is used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb620-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb620-118">Remarks</span></span>

<span data-ttu-id="cb620-119">Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="cb620-119">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="cb620-120">Você pode subclassear o controle de edição, mas não deve destruí-lo.</span><span class="sxs-lookup"><span data-stu-id="cb620-120">You can subclass the edit control, but you should not destroy it.</span></span>

<span data-ttu-id="cb620-121">O controle deve ter o foco antes de você enviar esta mensagem para o controle.</span><span class="sxs-lookup"><span data-stu-id="cb620-121">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="cb620-122">O foco pode ser definido usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="cb620-122">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

<span data-ttu-id="cb620-123">Se *wParam* for-1, um código de notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) será enviado.</span><span class="sxs-lookup"><span data-stu-id="cb620-123">If *wParam* is -1, an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification code is sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb620-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb620-124">Requirements</span></span>



| <span data-ttu-id="cb620-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb620-125">Requirement</span></span> | <span data-ttu-id="cb620-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cb620-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb620-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb620-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cb620-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb620-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb620-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb620-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cb620-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb620-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb620-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cb620-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb620-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb620-132"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="cb620-133">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cb620-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cb620-134">**LVM \_ EDITLABELW** (Unicode) e **LVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cb620-134">**LVM\_EDITLABELW** (Unicode) and **LVM\_EDITLABELA** (ANSI)</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="cb620-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cb620-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb620-136">**cancelamento do WM \_**</span><span class="sxs-lookup"><span data-stu-id="cb620-136">**WM\_CANCELMODE**</span></span>](/windows/desktop/winmsg/wm-cancelmode)
</dt> </dl>

 

