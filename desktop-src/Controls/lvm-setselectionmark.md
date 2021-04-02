---
title: Mensagem de LVM_SETSELECTIONMARK (commctrl. h)
description: Define a marca de seleção em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetSelectionMark do ListView.
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- Controles de LVM_SETSELECTIONMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644258"
---
# <a name="lvm_setselectionmark-message"></a><span data-ttu-id="c2fe8-105">\_Mensagem SETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="c2fe8-105">LVM\_SETSELECTIONMARK message</span></span>

<span data-ttu-id="c2fe8-106">Define a marca de seleção em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-106">Sets the selection mark in a list-view control.</span></span> <span data-ttu-id="c2fe8-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetSelectionMark do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="c2fe8-107">You can send this message explicitly or use the [**ListView\_SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2fe8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2fe8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2fe8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2fe8-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2fe8-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2fe8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2fe8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c2fe8-112">Índice de base zero da nova marca de seleção.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-112">Zero-based index of the new selection mark.</span></span> <span data-ttu-id="c2fe8-113">Se definido como-1, a marca de seleção será removida.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-113">If set to -1, the selection mark is removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2fe8-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2fe8-114">Return value</span></span>

<span data-ttu-id="c2fe8-115">Retorna a marca de seleção anterior ou-1 se não houver marca de seleção anterior.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-115">Returns the previous selection mark, or -1 if there is no previous selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2fe8-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2fe8-116">Remarks</span></span>

<span data-ttu-id="c2fe8-117">A *marca de seleção* é o índice de item do qual uma seleção múltipla é iniciada.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-117">The *selection mark* is the item index from which a multiple selection starts.</span></span> <span data-ttu-id="c2fe8-118">Esta mensagem não afeta o estado de seleção do item.</span><span class="sxs-lookup"><span data-stu-id="c2fe8-118">This message does not affect the selection state of the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2fe8-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2fe8-119">Requirements</span></span>



| <span data-ttu-id="c2fe8-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2fe8-120">Requirement</span></span> | <span data-ttu-id="c2fe8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c2fe8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2fe8-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2fe8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c2fe8-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2fe8-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2fe8-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2fe8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c2fe8-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2fe8-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2fe8-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2fe8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2fe8-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2fe8-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2fe8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2fe8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2fe8-129">**\_GETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="c2fe8-129">**LVM\_GETSELECTIONMARK**</span></span>](lvm-getselectionmark.md)
</dt> </dl>

 

 





