---
title: Mensagem de TVM_SETHOT (commctrl. h)
description: Define o item ativo para um controle de exibição de árvore. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetHot.
ms.assetid: 5e7368f5-40ce-4e7b-bbe3-5fe0b17181a8
keywords:
- Controles de TVM_SETHOT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETHOT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beccd5429267350682a6721cde66cca9316cf438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919017"
---
# <a name="tvm_sethot-message"></a><span data-ttu-id="dc967-105">\_Mensagem TVM SETHOT</span><span class="sxs-lookup"><span data-stu-id="dc967-105">TVM\_SETHOT message</span></span>

<span data-ttu-id="dc967-106">\[Destinado ao uso interno; Não recomendado para uso em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="dc967-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="dc967-107">Essa mensagem pode não ter suporte em versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc967-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="dc967-108">Define o item ativo para um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="dc967-108">Sets the hot item for a tree-view control.</span></span> <span data-ttu-id="dc967-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) .</span><span class="sxs-lookup"><span data-stu-id="dc967-109">You can send this message explicitly or by using the [**TreeView\_SetHot**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="dc967-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dc967-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc967-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc967-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc967-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="dc967-112">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="dc967-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc967-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc967-114">Identificador para o novo item ativo.</span><span class="sxs-lookup"><span data-stu-id="dc967-114">Handle to the new hot item.</span></span> <span data-ttu-id="dc967-115">Se esse valor for **nulo**, o controle de exibição de árvore será definido como sem item ativo.</span><span class="sxs-lookup"><span data-stu-id="dc967-115">If this value is **NULL**, the tree-view control will be set to have no hot item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc967-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dc967-116">Return value</span></span>

<span data-ttu-id="dc967-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="dc967-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="dc967-118">Considerações de segurança</span><span class="sxs-lookup"><span data-stu-id="dc967-118">Security Considerations</span></span>

<span data-ttu-id="dc967-119">O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="dc967-119">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc967-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc967-120">Remarks</span></span>

<span data-ttu-id="dc967-121">O *item ativo* é o item que o mouse está focalizando.</span><span class="sxs-lookup"><span data-stu-id="dc967-121">The *hot item* is the item that the mouse is hovering over.</span></span> <span data-ttu-id="dc967-122">Essa mensagem faz com que um item pareça ser o item ativo, mesmo que o mouse não esteja passando por ele.</span><span class="sxs-lookup"><span data-stu-id="dc967-122">This message makes an item look like it is the hot item even if the mouse is not hovering over it.</span></span>

<span data-ttu-id="dc967-123">Essa mensagem não terá efeito visível se o estilo de [**\_ TRACKSELECT de TVs**](tree-view-control-window-styles.md) não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="dc967-123">This message has no visible effect if the [**TVS\_TRACKSELECT**](tree-view-control-window-styles.md) style is not set.</span></span>

<span data-ttu-id="dc967-124">Se tiver sucesso, essa mensagem fará com que o item ativo seja redesenhado.</span><span class="sxs-lookup"><span data-stu-id="dc967-124">If it succeeds, this message causes the hot item to be redrawn.</span></span>

<span data-ttu-id="dc967-125">Essa mensagem será ignorada se *lParam* for **NULL** e o controle de exibição de árvore estiver acompanhando o mouse.</span><span class="sxs-lookup"><span data-stu-id="dc967-125">This message is ignored if *lParam* is **NULL** and the tree-view control is tracking the mouse.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc967-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc967-126">Requirements</span></span>



| <span data-ttu-id="dc967-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc967-127">Requirement</span></span> | <span data-ttu-id="dc967-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dc967-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc967-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc967-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dc967-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc967-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dc967-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc967-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dc967-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc967-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dc967-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc967-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc967-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc967-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc967-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc967-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc967-136">**\_SetHot TreeView**</span><span class="sxs-lookup"><span data-stu-id="dc967-136">**TreeView\_SetHot**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sethot)
</dt> </dl>

 

 





