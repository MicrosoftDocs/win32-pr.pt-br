---
title: Mensagem de LVM_GETSELECTIONMARK (commctrl. h)
description: Recupera a marca de seleção de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetSelectionMark do ListView.
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- Controles de LVM_GETSELECTIONMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753966"
---
# <a name="lvm_getselectionmark-message"></a><span data-ttu-id="13e00-105">\_Mensagem GETSELECTIONMARK LVM</span><span class="sxs-lookup"><span data-stu-id="13e00-105">LVM\_GETSELECTIONMARK message</span></span>

<span data-ttu-id="13e00-106">Recupera a marca de seleção de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="13e00-106">Retrieves the selection mark from a list-view control.</span></span> <span data-ttu-id="13e00-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetSelectionMark do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) .</span><span class="sxs-lookup"><span data-stu-id="13e00-107">You can send this message explicitly or use the [**ListView\_GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="13e00-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13e00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e00-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13e00-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="13e00-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="13e00-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="13e00-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13e00-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="13e00-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="13e00-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e00-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13e00-113">Return value</span></span>

<span data-ttu-id="13e00-114">Retorna a marca de seleção com base em zero ou-1 se não houver nenhuma marca de seleção.</span><span class="sxs-lookup"><span data-stu-id="13e00-114">Returns the zero-based selection mark, or -1 if there is no selection mark.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e00-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="13e00-115">Remarks</span></span>

<span data-ttu-id="13e00-116">A *marca de seleção* é o índice de item do qual uma seleção múltipla é iniciada.</span><span class="sxs-lookup"><span data-stu-id="13e00-116">The *selection mark* is the item index from which a multiple selection starts.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e00-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13e00-117">Requirements</span></span>



| <span data-ttu-id="13e00-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e00-118">Requirement</span></span> | <span data-ttu-id="13e00-119">Valor</span><span class="sxs-lookup"><span data-stu-id="13e00-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="13e00-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13e00-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13e00-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13e00-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13e00-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13e00-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13e00-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13e00-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="13e00-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13e00-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="13e00-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="13e00-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e00-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="13e00-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e00-127">**\_SETSELECTIONMARK LVM**</span><span class="sxs-lookup"><span data-stu-id="13e00-127">**LVM\_SETSELECTIONMARK**</span></span>](lvm-setselectionmark.md)
</dt> </dl>

 

 





