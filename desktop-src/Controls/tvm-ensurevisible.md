---
title: Mensagem de TVM_ENSUREVISIBLE (commctrl. h)
description: Garante que um item de exibição de árvore esteja visível, expandindo o item pai ou rolando o controle de exibição de árvore, se necessário. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ EnsureVisible.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- Controles de TVM_ENSUREVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06100ee33106736076608aa216d2aebc03b76ebe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918262"
---
# <a name="tvm_ensurevisible-message"></a><span data-ttu-id="8b128-105">\_Mensagem TVM ENSUREVISIBLE</span><span class="sxs-lookup"><span data-stu-id="8b128-105">TVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="8b128-106">Garante que um item de exibição de árvore esteja visível, expandindo o item pai ou rolando o controle de exibição de árvore, se necessário.</span><span class="sxs-lookup"><span data-stu-id="8b128-106">Ensures that a tree-view item is visible, expanding the parent item or scrolling the tree-view control, if necessary.</span></span> <span data-ttu-id="8b128-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="8b128-107">You can send this message explicitly or by using the [**TreeView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8b128-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b128-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b128-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8b128-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8b128-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8b128-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8b128-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8b128-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8b128-112">Identificador para o item.</span><span class="sxs-lookup"><span data-stu-id="8b128-112">Handle to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b128-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b128-113">Return value</span></span>

<span data-ttu-id="8b128-114">Retornará zero se o sistema tiver rolado os itens no controle de exibição em árvore e nenhum item tiver sido expandido.</span><span class="sxs-lookup"><span data-stu-id="8b128-114">Returns nonzero if the system scrolled the items in the tree-view control and no items were expanded.</span></span> <span data-ttu-id="8b128-115">Caso contrário, a mensagem retornará zero.</span><span class="sxs-lookup"><span data-stu-id="8b128-115">Otherwise, the message returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b128-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b128-116">Remarks</span></span>

<span data-ttu-id="8b128-117">Se a \_ mensagem TVM ENSUREVISIBLE expandir o item pai, a janela pai receberá os códigos de notificação de [TVN de \_ ](tvn-itemexpanded.md) TVN e itens de isexpanding. [ \_ ](tvn-itemexpanding.md)</span><span class="sxs-lookup"><span data-stu-id="8b128-117">If the TVM\_ENSUREVISIBLE message expands the parent item, the parent window receives the [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b128-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b128-118">Requirements</span></span>



| <span data-ttu-id="8b128-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b128-119">Requirement</span></span> | <span data-ttu-id="8b128-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8b128-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b128-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b128-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b128-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b128-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b128-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b128-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b128-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8b128-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8b128-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b128-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b128-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b128-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





