---
title: Mensagem de LVM_SETITEMSTATE (commctrl. h)
description: Altera o estado de um item em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetItemState do ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- Controles de LVM_SETITEMSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085637"
---
# <a name="lvm_setitemstate-message"></a><span data-ttu-id="6c8c8-105">Mensagem do LVM \_ SETitemstate</span><span class="sxs-lookup"><span data-stu-id="6c8c8-105">LVM\_SETITEMSTATE message</span></span>

<span data-ttu-id="6c8c8-106">Altera o estado de um item em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-106">Changes the state of an item in a list-view control.</span></span> <span data-ttu-id="6c8c8-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetItemState do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .</span><span class="sxs-lookup"><span data-stu-id="6c8c8-107">You can send this message explicitly or by using the [**ListView\_SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6c8c8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c8c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8c8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6c8c8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8c8-110">Índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-110">Index of the list-view item.</span></span> <span data-ttu-id="6c8c8-111">Se esse parâmetro for-1, a alteração de estado será aplicada a todos os itens.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-111">If this parameter is -1, then the state change is applied to all items.</span></span>

</dd> <dt>

<span data-ttu-id="6c8c8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c8c8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c8c8-113">Ponteiro para uma estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="6c8c8-113">Pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="6c8c8-114">O membro **stateMask** especifica quais bits de estado alterar e o membro de **estado** contém os novos valores para esses bits.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-114">The **stateMask** member specifies which state bits to change, and the **state** member contains the new values for those bits.</span></span> <span data-ttu-id="6c8c8-115">Os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-115">The other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8c8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c8c8-116">Return value</span></span>

<span data-ttu-id="6c8c8-117">Se você enviar essa mensagem explicitamente, ela retornará **true** se for bem-sucedida ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-117">If you send this message explicitly, it returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8c8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c8c8-118">Remarks</span></span>

<span data-ttu-id="6c8c8-119">O valor de estado de um item inclui um conjunto de sinalizadores de bits que indicam o estado do item.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-119">An item's state value includes a set of bit flags that indicate the item's state.</span></span> <span data-ttu-id="6c8c8-120">O valor de estado também pode incluir índices de lista de imagens que indicam a imagem de estado e a imagem de sobreposição do item.</span><span class="sxs-lookup"><span data-stu-id="6c8c8-120">The state value can also include image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8c8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c8c8-121">Requirements</span></span>



| <span data-ttu-id="6c8c8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8c8-122">Requirement</span></span> | <span data-ttu-id="6c8c8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6c8c8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8c8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c8c8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8c8-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c8c8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c8c8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c8c8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8c8-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6c8c8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c8c8-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c8c8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c8c8-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c8c8-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





