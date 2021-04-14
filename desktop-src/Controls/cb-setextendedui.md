---
title: Mensagem de CB_SETEXTENDEDUI (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de SETEXTENDEDUI CB para selecionar a interface do usuário padrão ou a interface do usuário estendida para uma caixa de combinação que tem o \_ estilo de lista suspensa CBS ou CBS \_ DROPDOWNLIST.
ms.assetid: c489e484-777e-4afa-996b-1ec3eb6552ab
keywords:
- Controles de CB_SETEXTENDEDUI de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETEXTENDEDUI
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f94c31c8bc5457799d0038ecd8340c03c55aed91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455119"
---
# <a name="cb_setextendedui-message"></a><span data-ttu-id="f213b-104">\_Mensagem de SETEXTENDEDUI CB</span><span class="sxs-lookup"><span data-stu-id="f213b-104">CB\_SETEXTENDEDUI message</span></span>

<span data-ttu-id="f213b-105">Um aplicativo envia uma mensagem de **\_ SETEXTENDEDUI CB** para selecionar a interface do usuário padrão ou a interface do usuário estendida para uma caixa de combinação que tem o estilo de [**\_ lista suspensa CBS**](combo-box-styles.md) ou [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f213b-105">An application sends a **CB\_SETEXTENDEDUI** message to select either the default UI or the extended UI for a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="f213b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f213b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f213b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f213b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f213b-108">Um **bool** que especifica se a caixa de combinação usa a interface do usuário estendida (**true**) ou a interface do usuário padrão (**false**).</span><span class="sxs-lookup"><span data-stu-id="f213b-108">A **BOOL** that specifies whether the combo box uses the extended UI (**TRUE**) or the default UI (**FALSE**).</span></span>

</dd> <dt>

<span data-ttu-id="f213b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f213b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f213b-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="f213b-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f213b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f213b-111">Return value</span></span>

<span data-ttu-id="f213b-112">Se a operação for concluída com sucesso, o valor de retorno será CB \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f213b-112">If the operation succeeds, the return value is CB\_OKAY.</span></span> <span data-ttu-id="f213b-113">Se ocorrer um erro, será CB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="f213b-113">If an error occurs, it is CB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="f213b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f213b-114">Remarks</span></span>

<span data-ttu-id="f213b-115">Por padrão, a tecla F4 é aberta ou fecha a lista e a seta para baixo altera a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="f213b-115">By default, the F4 key opens or closes the list and the DOWN ARROW changes the current selection.</span></span> <span data-ttu-id="f213b-116">Na interface do usuário estendida, a tecla F4 é desabilitada e a tecla de seta para baixo abre a lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="f213b-116">In the extended UI, the F4 key is disabled and the DOWN ARROW key opens the drop-down list.</span></span> <span data-ttu-id="f213b-117">A roda do mouse, que normalmente rola pelos itens da lista, não tem efeito quando a interface do usuário estendida está definida.</span><span class="sxs-lookup"><span data-stu-id="f213b-117">The mouse wheel, which normally scrolls through the items in the list, has no effect when the extended UI is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="f213b-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f213b-118">Requirements</span></span>



| <span data-ttu-id="f213b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f213b-119">Requirement</span></span> | <span data-ttu-id="f213b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f213b-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f213b-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f213b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f213b-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f213b-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f213b-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f213b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f213b-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f213b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f213b-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f213b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f213b-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f213b-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f213b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f213b-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f213b-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="f213b-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f213b-129">**\_GETEXTENDEDUI CB**</span><span class="sxs-lookup"><span data-stu-id="f213b-129">**CB\_GETEXTENDEDUI**</span></span>](cb-getextendedui.md)
</dt> <dt>

<span data-ttu-id="f213b-130">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="f213b-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f213b-131">Recursos da caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="f213b-131">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





