---
title: Mensagem de BM_SETCHECK (WinUser. h)
description: Define o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetCheck do botão.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Controles de BM_SETCHECK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008948"
---
# <a name="bm_setcheck-message"></a><span data-ttu-id="590a0-105">\_Mensagem BM SETcheck</span><span class="sxs-lookup"><span data-stu-id="590a0-105">BM\_SETCHECK message</span></span>

<span data-ttu-id="590a0-106">Define o estado de verificação de um botão de opção ou caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="590a0-106">Sets the check state of a radio button or check box.</span></span> <span data-ttu-id="590a0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetCheck do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .</span><span class="sxs-lookup"><span data-stu-id="590a0-107">You can send this message explicitly or by using the [**Button\_SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="590a0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="590a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="590a0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="590a0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="590a0-110">O estado de verificação.</span><span class="sxs-lookup"><span data-stu-id="590a0-110">The check state.</span></span> <span data-ttu-id="590a0-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="590a0-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="590a0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="590a0-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="590a0-113">Significado</span><span class="sxs-lookup"><span data-stu-id="590a0-113">Meaning</span></span>                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <span data-ttu-id="590a0-114"><dt>**BST \_ verificado**</dt></span><span class="sxs-lookup"><span data-stu-id="590a0-114"><dt>**BST\_CHECKED**</dt></span></span> </dl>                   | <span data-ttu-id="590a0-115">Define o estado do botão como marcado.</span><span class="sxs-lookup"><span data-stu-id="590a0-115">Sets the button state to checked.</span></span><br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <span data-ttu-id="590a0-116"><dt>**BST \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="590a0-116"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="590a0-117">Define o estado do botão como esmaecido, indicando um estado indeterminado.</span><span class="sxs-lookup"><span data-stu-id="590a0-117">Sets the button state to grayed, indicating an indeterminate state.</span></span> <span data-ttu-id="590a0-118">Use esse valor somente se o botão tiver o estilo [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="590a0-118">Use this value only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <span data-ttu-id="590a0-119"><dt>**BST não \_ verificado**</dt></span><span class="sxs-lookup"><span data-stu-id="590a0-119"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>             | <span data-ttu-id="590a0-120">Define o estado do botão como limpo.</span><span class="sxs-lookup"><span data-stu-id="590a0-120">Sets the button state to cleared.</span></span><br/>                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="590a0-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="590a0-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="590a0-122">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="590a0-122">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="590a0-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="590a0-123">Return value</span></span>

<span data-ttu-id="590a0-124">Essa mensagem sempre retorna zero.</span><span class="sxs-lookup"><span data-stu-id="590a0-124">This message always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="590a0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="590a0-125">Remarks</span></span>

<span data-ttu-id="590a0-126">A **mensagem \_ SetCheck BM** não tem efeito sobre botões de push.</span><span class="sxs-lookup"><span data-stu-id="590a0-126">The **BM\_SETCHECK** message has no effect on push buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="590a0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="590a0-127">Requirements</span></span>



| <span data-ttu-id="590a0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="590a0-128">Requirement</span></span> | <span data-ttu-id="590a0-129">Valor</span><span class="sxs-lookup"><span data-stu-id="590a0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="590a0-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="590a0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="590a0-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="590a0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="590a0-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="590a0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="590a0-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="590a0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="590a0-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="590a0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="590a0-135"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="590a0-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="590a0-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="590a0-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="590a0-137">**Referência**</span><span class="sxs-lookup"><span data-stu-id="590a0-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="590a0-138">**BM \_ GETcheck**</span><span class="sxs-lookup"><span data-stu-id="590a0-138">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="590a0-139">**BM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="590a0-139">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="590a0-140">**SetState BM \_**</span><span class="sxs-lookup"><span data-stu-id="590a0-140">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





