---
title: Mensagem de EM_SETSEL (WinUser. h)
description: Seleciona um intervalo de caracteres em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 5cb7ff1e-18e8-49c8-8072-872cf32b18b0
keywords:
- Controles de EM_SETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4981fa179ae4bdd454ab0b0a6d7485185ed31d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454940"
---
# <a name="em_setsel-message"></a><span data-ttu-id="8f7b5-105">\_Mensagem em SETSEL</span><span class="sxs-lookup"><span data-stu-id="8f7b5-105">EM\_SETSEL message</span></span>

<span data-ttu-id="8f7b5-106">Seleciona um intervalo de caracteres em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-106">Selects a range of characters in an edit control.</span></span> <span data-ttu-id="8f7b5-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f7b5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f7b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f7b5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f7b5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f7b5-110">A posição do caractere inicial da seleção.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-110">The starting character position of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="8f7b5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f7b5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f7b5-112">A posição do caractere final da seleção.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-112">The ending character position of the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f7b5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f7b5-113">Return value</span></span>

<span data-ttu-id="8f7b5-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f7b5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f7b5-115">Remarks</span></span>

<span data-ttu-id="8f7b5-116">O valor inicial pode ser maior que o valor final.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-116">The start value can be greater than the end value.</span></span> <span data-ttu-id="8f7b5-117">O menor dos dois valores especifica a posição do primeiro caractere na seleção.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-117">The lower of the two values specifies the character position of the first character in the selection.</span></span> <span data-ttu-id="8f7b5-118">O valor mais alto especifica a posição do primeiro caractere além da seleção.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-118">The higher value specifies the position of the first character beyond the selection.</span></span>

<span data-ttu-id="8f7b5-119">O valor inicial é o ponto de ancoragem da seleção e o valor final é a extremidade ativa.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-119">The start value is the anchor point of the selection, and the end value is the active end.</span></span> <span data-ttu-id="8f7b5-120">Se o usuário usar a tecla SHIFT para ajustar o tamanho da seleção, a extremidade ativa poderá ser movida, mas o ponto de ancoragem permanecerá o mesmo.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-120">If the user uses the SHIFT key to adjust the size of the selection, the active end can move but the anchor point remains the same.</span></span>

<span data-ttu-id="8f7b5-121">Se o início for 0 e o final for-1, todo o texto no controle de edição será selecionado.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-121">If the start is 0 and the end is -1, all the text in the edit control is selected.</span></span> <span data-ttu-id="8f7b5-122">Se o início for-1, qualquer seleção atual será desmarcada.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-122">If the start is -1, any current selection is deselected.</span></span>

<span data-ttu-id="8f7b5-123">**Controles de edição:** O controle exibe um cursor piscando na posição final, independentemente dos valores relativos de Start e end.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-123">**Edit controls:** The control displays a flashing caret at the end position regardless of the relative values of start and end.</span></span>

<span data-ttu-id="8f7b5-124">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-124">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="8f7b5-125">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="8f7b5-125">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="8f7b5-126">Se o controle de edição tiver o estilo [**es \_ NOHIDESEL**](edit-control-styles.md) , o texto selecionado será realçado, independentemente de o controle estar em foco.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-126">If the edit control has the [**ES\_NOHIDESEL**](edit-control-styles.md) style, the selected text is highlighted regardless of whether the control has focus.</span></span> <span data-ttu-id="8f7b5-127">Sem o estilo **es \_ NOHIDESEL** , o texto selecionado só é realçado quando o controle de edição tem o foco.</span><span class="sxs-lookup"><span data-stu-id="8f7b5-127">Without the **ES\_NOHIDESEL** style, the selected text is highlighted only when the edit control has the focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f7b5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f7b5-128">Requirements</span></span>



| <span data-ttu-id="8f7b5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f7b5-129">Requirement</span></span> | <span data-ttu-id="8f7b5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8f7b5-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f7b5-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f7b5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8f7b5-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f7b5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8f7b5-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f7b5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8f7b5-134">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f7b5-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8f7b5-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f7b5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f7b5-136"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8f7b5-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f7b5-137">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8f7b5-137">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f7b5-138">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8f7b5-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8f7b5-139">**em \_ GETSEL**</span><span class="sxs-lookup"><span data-stu-id="8f7b5-139">**EM\_GETSEL**</span></span>](em-getsel.md)
</dt> <dt>

[<span data-ttu-id="8f7b5-140">**em \_ REPLACESEL**</span><span class="sxs-lookup"><span data-stu-id="8f7b5-140">**EM\_REPLACESEL**</span></span>](em-replacesel.md)
</dt> <dt>

[<span data-ttu-id="8f7b5-141">**em \_ SCROLLCARET**</span><span class="sxs-lookup"><span data-stu-id="8f7b5-141">**EM\_SCROLLCARET**</span></span>](em-scrollcaret.md)
</dt> <dt>

[<span data-ttu-id="8f7b5-142">**em \_ EXSETSEL**</span><span class="sxs-lookup"><span data-stu-id="8f7b5-142">**EM\_EXSETSEL**</span></span>](em-exsetsel.md)
</dt> </dl>

 

 





