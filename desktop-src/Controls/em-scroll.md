---
title: Mensagem de EM_SCROLL (WinUser. h)
description: Rola o texto verticalmente em um controle de edição de várias linhas. Essa mensagem é equivalente a enviar uma \_ mensagem do WM VSCROLL para o controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Controles de EM_SCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086418"
---
# <a name="em_scroll-message"></a><span data-ttu-id="a232b-106">\_Mensagem de rolagem em em</span><span class="sxs-lookup"><span data-stu-id="a232b-106">EM\_SCROLL message</span></span>

<span data-ttu-id="a232b-107">Rola o texto verticalmente em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="a232b-107">Scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="a232b-108">Essa mensagem é equivalente a enviar uma mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) para o controle de edição.</span><span class="sxs-lookup"><span data-stu-id="a232b-108">This message is equivalent to sending a [**WM\_VSCROLL**](wm-vscroll.md) message to the edit control.</span></span> <span data-ttu-id="a232b-109">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="a232b-109">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a232b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a232b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a232b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a232b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a232b-112">A ação que a barra de rolagem deve tomar.</span><span class="sxs-lookup"><span data-stu-id="a232b-112">The action the scroll bar is to take.</span></span> <span data-ttu-id="a232b-113">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a232b-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a232b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a232b-114">Value</span></span>                                                                                                                                                   | <span data-ttu-id="a232b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a232b-115">Meaning</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="a232b-116"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="a232b-116"><dt>**SB\_LINEDOWN**</dt></span></span> </dl> | <span data-ttu-id="a232b-117">Rola uma linha para baixo.</span><span class="sxs-lookup"><span data-stu-id="a232b-117">Scrolls down one line.</span></span><br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="a232b-118"><dt>**linha de SB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a232b-118"><dt>**SB\_LINEUP**</dt></span></span> </dl>       | <span data-ttu-id="a232b-119">Rola uma linha para cima.</span><span class="sxs-lookup"><span data-stu-id="a232b-119">Scrolls up one line.</span></span><br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="a232b-120"><dt>**SB \_ PageDown**</dt></span><span class="sxs-lookup"><span data-stu-id="a232b-120"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl> | <span data-ttu-id="a232b-121">Rola uma página para baixo.</span><span class="sxs-lookup"><span data-stu-id="a232b-121">Scrolls down one page.</span></span><br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="a232b-122"><dt>**SB \_ PageUp**</dt></span><span class="sxs-lookup"><span data-stu-id="a232b-122"><dt>**SB\_PAGEUP**</dt></span></span> </dl>       | <span data-ttu-id="a232b-123">Rola uma página para cima.</span><span class="sxs-lookup"><span data-stu-id="a232b-123">Scrolls up one page.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="a232b-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a232b-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a232b-125">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a232b-125">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a232b-126">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a232b-126">Return value</span></span>

<span data-ttu-id="a232b-127">Se a mensagem for bem-sucedida, o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) do valor de retorno será **true** e [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) será o número de linhas que o comando rolará.</span><span class="sxs-lookup"><span data-stu-id="a232b-127">If the message is successful, the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the return value is **TRUE**, and the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the number of lines that the command scrolls.</span></span> <span data-ttu-id="a232b-128">O número retornado pode não ser o mesmo que o número real de linhas roladas se a rolagem for movida para o início ou para o fim do texto.</span><span class="sxs-lookup"><span data-stu-id="a232b-128">The number returned may not be the same as the actual number of lines scrolled if the scrolling moves to the beginning or the end of the text.</span></span> <span data-ttu-id="a232b-129">Se o parâmetro *wParam* especificar um valor inválido, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="a232b-129">If the *wParam* parameter specifies an invalid value, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a232b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a232b-130">Remarks</span></span>

<span data-ttu-id="a232b-131">Para rolar para uma linha ou posição de caractere específica, use a mensagem em [**\_ LINESCROLL**](em-linescroll.md) .</span><span class="sxs-lookup"><span data-stu-id="a232b-131">To scroll to a specific line or character position, use the [**EM\_LINESCROLL**](em-linescroll.md) message.</span></span> <span data-ttu-id="a232b-132">Para rolar o cursor para a exibição, use a mensagem em [**\_ SCROLLCARET**](em-scrollcaret.md) .</span><span class="sxs-lookup"><span data-stu-id="a232b-132">To scroll the caret into view, use the [**EM\_SCROLLCARET**](em-scrollcaret.md) message.</span></span>

<span data-ttu-id="a232b-133">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a232b-133">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="a232b-134">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="a232b-134">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a232b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a232b-135">Requirements</span></span>



| <span data-ttu-id="a232b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a232b-136">Requirement</span></span> | <span data-ttu-id="a232b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="a232b-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a232b-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a232b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a232b-139">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a232b-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a232b-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a232b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a232b-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a232b-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a232b-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a232b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="a232b-143"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a232b-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a232b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="a232b-144">See also</span></span>

<dl> <dt>

<span data-ttu-id="a232b-145">**Referência**</span><span class="sxs-lookup"><span data-stu-id="a232b-145">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a232b-146">**em \_ LINESCROLL**</span><span class="sxs-lookup"><span data-stu-id="a232b-146">**EM\_LINESCROLL**</span></span>](em-linescroll.md)
</dt> <dt>

[<span data-ttu-id="a232b-147">**em \_ SCROLLCARET**</span><span class="sxs-lookup"><span data-stu-id="a232b-147">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="a232b-148">**VSCROLL do WM \_**</span><span class="sxs-lookup"><span data-stu-id="a232b-148">**WM\_VSCROLL**</span></span>](wm-vscroll.md)
</dt> </dl>

 

