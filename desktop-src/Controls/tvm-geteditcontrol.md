---
title: Mensagem de TVM_GETEDITCONTROL (commctrl. h)
description: Recupera o identificador para o controle de edição usado para editar um texto do item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ GetEditControl.
ms.assetid: c89e57e8-e113-47a1-85e6-bb68990f9c1a
keywords:
- Controles de TVM_GETEDITCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b4ce0beb125218e65c2c342caf59b57473088e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086316"
---
# <a name="tvm_geteditcontrol-message"></a><span data-ttu-id="3b7e1-105">\_Mensagem TVM GETEDITCONTROL</span><span class="sxs-lookup"><span data-stu-id="3b7e1-105">TVM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="3b7e1-106">Recupera o identificador para o controle de edição usado para editar um texto do item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-106">Retrieves the handle to the edit control being used to edit a tree-view item's text.</span></span> <span data-ttu-id="3b7e1-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) .</span><span class="sxs-lookup"><span data-stu-id="3b7e1-107">You can send this message explicitly or by using the [**TreeView\_GetEditControl**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_geteditcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3b7e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b7e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b7e1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3b7e1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3b7e1-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3b7e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3b7e1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3b7e1-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b7e1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b7e1-113">Return value</span></span>

<span data-ttu-id="3b7e1-114">Retorna o identificador para o controle de edição, se for bem-sucedido, ou **NULL** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-114">Returns the handle to the edit control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b7e1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b7e1-115">Remarks</span></span>

<span data-ttu-id="3b7e1-116">Quando o rótulo é iniciado, um controle de edição é criado, mas não posicionado ou exibido.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-116">When label editing begins, an edit control is created, but not positioned or displayed.</span></span> <span data-ttu-id="3b7e1-117">Antes de ser exibida, o controle de exibição de árvore envia a janela pai um código de notificação [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) .</span><span class="sxs-lookup"><span data-stu-id="3b7e1-117">Before it is displayed, the tree-view control sends its parent window an [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code.</span></span>

<span data-ttu-id="3b7e1-118">Para personalizar a edição de rótulo, implemente um manipulador para [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) e envie uma mensagem **TVM \_ GETEDITCONTROL** para o controle de exibição em árvore.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-118">To customize label editing, implement a handler for [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) and have it send a **TVM\_GETEDITCONTROL** message to the tree-view control.</span></span> <span data-ttu-id="3b7e1-119">Se um rótulo estiver sendo editado, o valor de retorno será um identificador para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="3b7e1-119">If a label is being edited, the return value will be a handle to the edit control.</span></span> <span data-ttu-id="3b7e1-120">Use esse identificador para personalizar o controle de edição enviando as mensagens usuais em **\_ xxx** .</span><span class="sxs-lookup"><span data-stu-id="3b7e1-120">Use this handle to customize the edit control by sending the usual **EM\_XXX** messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b7e1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b7e1-121">Requirements</span></span>



| <span data-ttu-id="3b7e1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b7e1-122">Requirement</span></span> | <span data-ttu-id="3b7e1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3b7e1-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b7e1-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b7e1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3b7e1-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b7e1-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3b7e1-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b7e1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3b7e1-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b7e1-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3b7e1-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b7e1-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b7e1-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b7e1-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





