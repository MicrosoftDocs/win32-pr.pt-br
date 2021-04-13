---
title: Mensagem de TVM_ENDEDITLABELNOW (commctrl. h)
description: Finaliza a edição de um rótulo de item de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ EndEditLabelNow.
ms.assetid: 68de2020-9311-4958-859a-de55f5e41fcf
keywords:
- Controles de TVM_ENDEDITLABELNOW de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_ENDEDITLABELNOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f059be20560adeb8cbcb0c63a2555283f6b7051
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499311"
---
# <a name="tvm_endeditlabelnow-message"></a><span data-ttu-id="85d08-105">\_Mensagem TVM ENDEDITLABELNOW</span><span class="sxs-lookup"><span data-stu-id="85d08-105">TVM\_ENDEDITLABELNOW message</span></span>

<span data-ttu-id="85d08-106">Finaliza a edição de um rótulo de item de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="85d08-106">Ends the editing of a tree-view item's label.</span></span> <span data-ttu-id="85d08-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) .</span><span class="sxs-lookup"><span data-stu-id="85d08-107">You can send this message explicitly or by using the [**TreeView\_EndEditLabelNow**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_endeditlabelnow) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="85d08-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="85d08-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85d08-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85d08-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85d08-110">Variável que indica se a edição é cancelada sem ser salva no rótulo.</span><span class="sxs-lookup"><span data-stu-id="85d08-110">Variable that indicates whether the editing is canceled without being saved to the label.</span></span> <span data-ttu-id="85d08-111">Se esse parâmetro for **true**, o sistema cancelará a edição sem salvar as alterações.</span><span class="sxs-lookup"><span data-stu-id="85d08-111">If this parameter is **TRUE**, the system cancels editing without saving the changes.</span></span> <span data-ttu-id="85d08-112">Caso contrário, o sistema salvará as alterações no rótulo.</span><span class="sxs-lookup"><span data-stu-id="85d08-112">Otherwise, the system saves the changes to the label.</span></span>

</dd> <dt>

<span data-ttu-id="85d08-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85d08-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="85d08-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="85d08-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85d08-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="85d08-115">Return value</span></span>

<span data-ttu-id="85d08-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="85d08-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="85d08-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="85d08-117">Remarks</span></span>

<span data-ttu-id="85d08-118">Essa mensagem faz com que o código de notificação [TVN \_ ENDLABELEDIT](tvn-endlabeledit.md) seja enviado para a janela pai do controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="85d08-118">This message causes the [TVN\_ENDLABELEDIT](tvn-endlabeledit.md) notification code to be sent to the parent window of the tree-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="85d08-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85d08-119">Requirements</span></span>



| <span data-ttu-id="85d08-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85d08-120">Requirement</span></span> | <span data-ttu-id="85d08-121">Valor</span><span class="sxs-lookup"><span data-stu-id="85d08-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85d08-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85d08-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85d08-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85d08-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85d08-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85d08-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85d08-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="85d08-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85d08-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="85d08-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="85d08-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85d08-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





