---
title: Mensagem de LVM_GETEDITCONTROL (commctrl. h)
description: Obtém o identificador para o controle de edição usado para editar o texto de um item de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetEditControl do ListView.
ms.assetid: 70450b24-9879-4be8-9bc9-f87008b66415
keywords:
- Controles de LVM_GETEDITCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a8790f86fee17f72078f61899edcd79b331759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008865"
---
# <a name="lvm_geteditcontrol-message"></a><span data-ttu-id="8cabe-105">\_Mensagem GETEDITCONTROL LVM</span><span class="sxs-lookup"><span data-stu-id="8cabe-105">LVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="8cabe-106">Obtém o identificador para o controle de edição usado para editar o texto de um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="8cabe-106">Gets the handle to the edit control being used to edit a list-view item's text.</span></span> <span data-ttu-id="8cabe-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetEditControl do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="8cabe-107">You can send this message explicitly or by using the [**ListView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8cabe-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8cabe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cabe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8cabe-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8cabe-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8cabe-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8cabe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8cabe-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8cabe-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8cabe-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cabe-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8cabe-113">Return value</span></span>

<span data-ttu-id="8cabe-114">Retorna o identificador para o controle de edição, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8cabe-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cabe-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cabe-115">Remarks</span></span>

<span data-ttu-id="8cabe-116">Quando o rótulo é iniciado, um controle de edição é criado, posicionado e inicializado.</span><span class="sxs-lookup"><span data-stu-id="8cabe-116">When label editing begins, an edit control is created, positioned, and initialized.</span></span> <span data-ttu-id="8cabe-117">Antes de ser exibida, o controle List-View envia à janela pai um código de notificação [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="8cabe-117">Before it is displayed, the list-view control sends its parent window an [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="8cabe-118">Para personalizar a edição de rótulo, implemente um manipulador para [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) e envie uma mensagem de **\_ GETEDITCONTROL LVM** para o controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="8cabe-118">To customize label editing, implement a handler for [LVN\_BEGINLABELEDIT](lvn-beginlabeledit.md) and have it send an **LVM\_GETEDITCONTROL** message to the list-view control.</span></span> <span data-ttu-id="8cabe-119">Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8cabe-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="8cabe-120">Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em **\_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="8cabe-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

<span data-ttu-id="8cabe-121">Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="8cabe-121">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="8cabe-122">Você pode subclassear o controle de edição, mas não deve destruí-lo.</span><span class="sxs-lookup"><span data-stu-id="8cabe-122">You can subclass the edit control, but you should not destroy it.</span></span> <span data-ttu-id="8cabe-123">Para cancelar a edição, envie o controle de exibição de lista para uma mensagem do [**WM \_ cancelable**](/windows/desktop/winmsg/wm-cancelmode) .</span><span class="sxs-lookup"><span data-stu-id="8cabe-123">To cancel editing, send the list-view control a [**WM\_CANCELMODE**](/windows/desktop/winmsg/wm-cancelmode) message.</span></span>

<span data-ttu-id="8cabe-124">O item de exibição de lista que está sendo editado é o item atualmente focalizado, que é o item no estado focalizado.</span><span class="sxs-lookup"><span data-stu-id="8cabe-124">The list-view item being edited is the currently focused item that is, the item in the focused state.</span></span> <span data-ttu-id="8cabe-125">Para localizar um item com base em seu estado, use a mensagem [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) .</span><span class="sxs-lookup"><span data-stu-id="8cabe-125">To find an item based on its state, use the [**LVM\_GETNEXTITEM**](lvm-getnextitem.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cabe-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cabe-126">Requirements</span></span>



| <span data-ttu-id="8cabe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cabe-127">Requirement</span></span> | <span data-ttu-id="8cabe-128">Valor</span><span class="sxs-lookup"><span data-stu-id="8cabe-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8cabe-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cabe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8cabe-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8cabe-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8cabe-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cabe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8cabe-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8cabe-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8cabe-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cabe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cabe-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cabe-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cabe-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cabe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cabe-136">**GetEditControl de ListView \_**</span><span class="sxs-lookup"><span data-stu-id="8cabe-136">**ListView\_GetEditControl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-listview_geteditcontrol)
</dt> </dl>

 

