---
title: Mensagem de BM_GETSTATE (WinUser. h)
description: Recupera o estado de um botão ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetState do botão.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Controles de BM_GETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918042"
---
# <a name="bm_getstate-message"></a><span data-ttu-id="38ac6-105">\_Mensagem GETstate do BM</span><span class="sxs-lookup"><span data-stu-id="38ac6-105">BM\_GETSTATE message</span></span>

<span data-ttu-id="38ac6-106">Recupera o estado de um botão ou caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="38ac6-106">Retrieves the state of a button or check box.</span></span> <span data-ttu-id="38ac6-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetState do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .</span><span class="sxs-lookup"><span data-stu-id="38ac6-107">You can send this message explicitly or use the [**Button\_GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="38ac6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38ac6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ac6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38ac6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ac6-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="38ac6-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="38ac6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ac6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38ac6-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="38ac6-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ac6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38ac6-113">Return value</span></span>

<span data-ttu-id="38ac6-114">O valor de retorno especifica o estado atual do botão.</span><span class="sxs-lookup"><span data-stu-id="38ac6-114">The return value specifies the current state of the button.</span></span> <span data-ttu-id="38ac6-115">É uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="38ac6-115">It is a combination of the following values.</span></span>



| <span data-ttu-id="38ac6-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="38ac6-116">Return code</span></span>                                                                                        | <span data-ttu-id="38ac6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="38ac6-117">Description</span></span>                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38ac6-118"><dt>**BST \_ verificado**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-118"><dt>**BST\_CHECKED**</dt></span></span> </dl>        | <span data-ttu-id="38ac6-119">O botão está marcado.</span><span class="sxs-lookup"><span data-stu-id="38ac6-119">The button is checked.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="38ac6-120"><dt>**BST \_ DROPDOWNPUSHED**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-120"><dt>**BST\_DROPDOWNPUSHED**</dt></span></span> </dl> | <span data-ttu-id="38ac6-121">[Windows Vista](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="38ac6-121">[Windows Vista](common-control-versions.md).</span></span> <span data-ttu-id="38ac6-122">O botão está no estado suspenso.</span><span class="sxs-lookup"><span data-stu-id="38ac6-122">The button is in the drop-down state.</span></span> <span data-ttu-id="38ac6-123">Aplica-se somente se o botão tiver o estilo [**\_ suspenso TBSTYLE**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="38ac6-123">Applies only if the button has the [**TBSTYLE\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span><br/> |
| <dl> <span data-ttu-id="38ac6-124"><dt>**foco de BST \_**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-124"><dt>**BST\_FOCUS**</dt></span></span> </dl>          | <span data-ttu-id="38ac6-125">O botão tem o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="38ac6-125">The button has the keyboard focus.</span></span><br/>                                                                                                                                                                            |
| <dl> <span data-ttu-id="38ac6-126"><dt>**BST \_ quente**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-126"><dt>**BST\_HOT**</dt></span></span> </dl>            | <span data-ttu-id="38ac6-127">O botão está quente; ou seja, o mouse está focalizando-o.</span><span class="sxs-lookup"><span data-stu-id="38ac6-127">The button is hot; that is, the mouse is hovering over it.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="38ac6-128"><dt>**BST \_ indeterminado**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-128"><dt>**BST\_INDETERMINATE**</dt></span></span> </dl>  | <span data-ttu-id="38ac6-129">O estado do botão é indeterminado.</span><span class="sxs-lookup"><span data-stu-id="38ac6-129">The state of the button is indeterminate.</span></span> <span data-ttu-id="38ac6-130">Aplica-se somente se o botão tiver o estilo [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="38ac6-130">Applies only if the button has the [**BS\_3STATE**](button-styles.md) or [**BS\_AUTO3STATE**](button-styles.md) style.</span></span><br/>                    |
| <dl> <span data-ttu-id="38ac6-131"><dt>**BST \_ enviado por push**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-131"><dt>**BST\_PUSHED**</dt></span></span> </dl>         | <span data-ttu-id="38ac6-132">O botão está sendo exibido no estado enviado por push.</span><span class="sxs-lookup"><span data-stu-id="38ac6-132">The button is being shown in the pushed state.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="38ac6-133"><dt>**BST não \_ verificado**</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-133"><dt>**BST\_UNCHECKED**</dt></span></span> </dl>      | <span data-ttu-id="38ac6-134">Nenhum estado especial.</span><span class="sxs-lookup"><span data-stu-id="38ac6-134">No special state.</span></span> <span data-ttu-id="38ac6-135">Equivalente a zero.</span><span class="sxs-lookup"><span data-stu-id="38ac6-135">Equivalent to zero.</span></span><br/>                                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="38ac6-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ac6-136">Requirements</span></span>



| <span data-ttu-id="38ac6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ac6-137">Requirement</span></span> | <span data-ttu-id="38ac6-138">Valor</span><span class="sxs-lookup"><span data-stu-id="38ac6-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38ac6-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38ac6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="38ac6-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38ac6-140">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="38ac6-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38ac6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="38ac6-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38ac6-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="38ac6-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38ac6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="38ac6-144"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38ac6-144"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ac6-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="38ac6-145">See also</span></span>

<dl> <dt>

<span data-ttu-id="38ac6-146">**Referência**</span><span class="sxs-lookup"><span data-stu-id="38ac6-146">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38ac6-147">**BM \_ GETcheck**</span><span class="sxs-lookup"><span data-stu-id="38ac6-147">**BM\_GETCHECK**</span></span>](bm-getcheck.md)
</dt> <dt>

[<span data-ttu-id="38ac6-148">**SetState BM \_**</span><span class="sxs-lookup"><span data-stu-id="38ac6-148">**BM\_SETSTATE**</span></span>](bm-setstate.md)
</dt> </dl>

 

 





