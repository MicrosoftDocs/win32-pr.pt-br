---
title: Mensagem de TVM_EDITLABEL (commctrl. h)
description: Inicia a edição in-loco do texto do item especificado, substituindo o texto do item por um controle de edição de linha única que contém o texto.
ms.assetid: ae844cbf-fa43-4f91-90cc-688f44bf77a5
keywords:
- Controles de TVM_EDITLABEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_EDITLABEL
- TVM_EDITLABELA
- TVM_EDITLABELW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3608c3f959c45571d9bc085518b763cf505180ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918263"
---
# <a name="tvm_editlabel-message"></a><span data-ttu-id="ced3f-104">\_Mensagem TVM EDITLABEL</span><span class="sxs-lookup"><span data-stu-id="ced3f-104">TVM\_EDITLABEL message</span></span>

<span data-ttu-id="ced3f-105">Inicia a edição in-loco do texto do item especificado, substituindo o texto do item por um controle de edição de linha única que contém o texto.</span><span class="sxs-lookup"><span data-stu-id="ced3f-105">Begins in-place editing of the specified item's text, replacing the text of the item with a single-line edit control containing the text.</span></span> <span data-ttu-id="ced3f-106">Essa mensagem seleciona implicitamente e concentra o item especificado.</span><span class="sxs-lookup"><span data-stu-id="ced3f-106">This message implicitly selects and focuses the specified item.</span></span> <span data-ttu-id="ced3f-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) .</span><span class="sxs-lookup"><span data-stu-id="ced3f-107">You can send this message explicitly or by using the [**TreeView\_EditLabel**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_editlabel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ced3f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ced3f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ced3f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ced3f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ced3f-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ced3f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ced3f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ced3f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ced3f-112">Identificador para o item a ser editado.</span><span class="sxs-lookup"><span data-stu-id="ced3f-112">Handle to the item to edit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ced3f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ced3f-113">Return value</span></span>

<span data-ttu-id="ced3f-114">Retorna o identificador para o controle de edição usado para editar o texto do item, se for bem-sucedido, ou **NULL** de outra forma.</span><span class="sxs-lookup"><span data-stu-id="ced3f-114">Returns the handle to the edit control used to edit the item text if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ced3f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ced3f-115">Remarks</span></span>

<span data-ttu-id="ced3f-116">Essa mensagem envia um código de notificação [TVN \_ BEGINLABELEDIT](tvn-beginlabeledit.md) para o pai do controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="ced3f-116">This message sends a [TVN\_BEGINLABELEDIT](tvn-beginlabeledit.md) notification code to the parent of the tree-view control.</span></span>

<span data-ttu-id="ced3f-117">Quando o usuário conclui ou cancela a edição, o controle de edição é destruído e o identificador não é mais válido.</span><span class="sxs-lookup"><span data-stu-id="ced3f-117">When the user completes or cancels editing, the edit control is destroyed and the handle is no longer valid.</span></span> <span data-ttu-id="ced3f-118">Você pode subclassear o controle de edição, mas não destruí-lo.</span><span class="sxs-lookup"><span data-stu-id="ced3f-118">You can subclass the edit control, but do not destroy it.</span></span>

<span data-ttu-id="ced3f-119">O controle deve ter o foco antes de você enviar esta mensagem para o controle.</span><span class="sxs-lookup"><span data-stu-id="ced3f-119">The control must have the focus before you send this message to the control.</span></span> <span data-ttu-id="ced3f-120">O foco pode ser definido usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="ced3f-120">Focus can be set using the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ced3f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ced3f-121">Requirements</span></span>



| <span data-ttu-id="ced3f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ced3f-122">Requirement</span></span> | <span data-ttu-id="ced3f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ced3f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ced3f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ced3f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ced3f-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ced3f-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ced3f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ced3f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ced3f-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ced3f-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ced3f-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ced3f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ced3f-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ced3f-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ced3f-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ced3f-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ced3f-131">**TVM \_ EDITLABELW** (Unicode) e **TVM \_ EDITLABELA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ced3f-131">**TVM\_EDITLABELW** (Unicode) and **TVM\_EDITLABELA** (ANSI)</span></span><br/>               |



 

