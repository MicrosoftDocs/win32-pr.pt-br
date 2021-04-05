---
title: Mensagem de BM_GETCHECK (WinUser. h)
description: Obtém o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar o botão \_ getcheck macro.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Controles de BM_GETCHECK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086252"
---
# <a name="bm_getcheck-message"></a><span data-ttu-id="b4b9c-105">Mensagem de BM \_ GETcheck</span><span class="sxs-lookup"><span data-stu-id="b4b9c-105">BM\_GETCHECK message</span></span>

<span data-ttu-id="b4b9c-106">Obtém o estado de verificação de um botão de opção ou caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-106">Gets the check state of a radio button or check box.</span></span> <span data-ttu-id="b4b9c-107">Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-107">You can send this message explicitly or use the [**Button\_GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4b9c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4b9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b9c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4b9c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4b9c-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b4b9c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4b9c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4b9c-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b9c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4b9c-113">Return value</span></span>

<span data-ttu-id="b4b9c-114">O valor de retorno de um botão criado com o estilo [**\_ AUTOCHECKBOX BS**](button-styles.md), [**BS \_ AUTORADIOBUTTON**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), [**BS \_ CheckBox**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)ou [**BS \_ 3STATE**](button-styles.md) pode ser um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-114">The return value from a button created with the [**BS\_AUTOCHECKBOX**](button-styles.md), [**BS\_AUTORADIOBUTTON**](button-styles.md), [**BS\_AUTO3STATE**](button-styles.md), [**BS\_CHECKBOX**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), or [**BS\_3STATE**](button-styles.md) style can be one of the following.</span></span>



| <span data-ttu-id="b4b9c-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b4b9c-115">Return code</span></span>                                                                                       | <span data-ttu-id="b4b9c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4b9c-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4b9c-117"><dt>**BST \_ verificado**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b9c-117"><dt>**BST\_CHECKED**</dt></span></span> </dl>       | <span data-ttu-id="b4b9c-118">O botão está marcado.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-118">Button is checked.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="b4b9c-119"><dt>**BST \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b9c-119"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl> | <span data-ttu-id="b4b9c-120">O botão fica acinzentado, indicando um estado indeterminado (aplica-se somente se o botão tiver o estilo [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) ).</span><span class="sxs-lookup"><span data-stu-id="b4b9c-120">Button is grayed, indicating an indeterminate state (applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style).</span></span><br/> |
| <dl> <span data-ttu-id="b4b9c-121"><dt>**BST não \_ verificado**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b9c-121"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>     | <span data-ttu-id="b4b9c-122">O botão está desmarcado</span><span class="sxs-lookup"><span data-stu-id="b4b9c-122">Button is cleared</span></span><br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b4b9c-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4b9c-123">Remarks</span></span>

<span data-ttu-id="b4b9c-124">Se o botão tiver um estilo diferente daqueles listados, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-124">If the button has a style other than those listed, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b9c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4b9c-125">Requirements</span></span>



| <span data-ttu-id="b4b9c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b9c-126">Requirement</span></span> | <span data-ttu-id="b4b9c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="b4b9c-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b9c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4b9c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b9c-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4b9c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b4b9c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4b9c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b9c-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4b9c-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b4b9c-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4b9c-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b9c-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4b9c-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b9c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4b9c-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="b4b9c-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="b4b9c-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b4b9c-136">**BM \_ GETstate**</span><span class="sxs-lookup"><span data-stu-id="b4b9c-136">**BM\_GETSTATE**</span></span>](bm-getstate.md)
</dt> <dt>

[<span data-ttu-id="b4b9c-137">**BM \_ SETcheck**</span><span class="sxs-lookup"><span data-stu-id="b4b9c-137">**BM\_SETCHECK**</span></span>](bm-setcheck.md)
</dt> </dl>

 

 





