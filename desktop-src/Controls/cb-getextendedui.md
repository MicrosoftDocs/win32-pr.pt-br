---
title: Mensagem de CB_GETEXTENDEDUI (WinUser. h)
description: Determina se uma caixa de combinação tem a interface do usuário padrão ou a interface do usuário estendida.
ms.assetid: 4f5580e0-68b1-4584-bf79-561fb8222fe0
keywords:
- Controles de CB_GETEXTENDEDUI de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94d90550bf341fc8586174c7ec57eb77fad08c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455126"
---
# <a name="cb_getextendedui-message"></a><span data-ttu-id="08060-104">\_Mensagem de GETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="08060-104">CB\_GETEXTENDEDUI message</span></span>

<span data-ttu-id="08060-105">Determina se uma caixa de combinação tem a interface do usuário padrão ou a interface do usuário estendida.</span><span class="sxs-lookup"><span data-stu-id="08060-105">Determines whether a combo box has the default user interface or the extended user interface.</span></span>

## <a name="parameters"></a><span data-ttu-id="08060-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08060-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08060-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08060-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="08060-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="08060-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08060-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08060-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="08060-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08060-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08060-111">Return value</span></span>

<span data-ttu-id="08060-112">Se a caixa de combinação tiver a interface do usuário estendida, o valor de retorno será **true**; caso contrário, será **false**.</span><span class="sxs-lookup"><span data-stu-id="08060-112">If the combo box has the extended user interface, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="08060-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="08060-113">Remarks</span></span>

<span data-ttu-id="08060-114">Por padrão, a tecla F4 é aberta ou fecha a lista e a seta para baixo altera a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="08060-114">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="08060-115">Em uma caixa de combinação com a interface do usuário estendida, a tecla F4 é desabilitada e pressionar a tecla de seta para baixo abre a lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="08060-115">In a combo box with the extended user interface, the F4 key is disabled and pressing the DOWN ARROW key opens the drop-down list.</span></span>

## <a name="requirements"></a><span data-ttu-id="08060-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08060-116">Requirements</span></span>



| <span data-ttu-id="08060-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="08060-117">Requirement</span></span> | <span data-ttu-id="08060-118">Valor</span><span class="sxs-lookup"><span data-stu-id="08060-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08060-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08060-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08060-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08060-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="08060-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08060-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08060-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08060-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08060-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="08060-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08060-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08060-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08060-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="08060-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="08060-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="08060-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="08060-127">**\_SETEXTENDEDUI CB**</span><span class="sxs-lookup"><span data-stu-id="08060-127">**CB\_SETEXTENDEDUI**</span></span>](cb-setextendedui.md)
</dt> <dt>

<span data-ttu-id="08060-128">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="08060-128">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="08060-129">Recursos da caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="08060-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





