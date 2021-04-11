---
title: Mensagem de EM_REPLACESEL (WinUser. h)
description: Substitui o texto selecionado em um controle de edição ou um controle de edição rico pelo texto especificado.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- Controles de EM_REPLACESEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086419"
---
# <a name="em_replacesel-message"></a><span data-ttu-id="ddbee-104">\_Mensagem em REPLACESEL</span><span class="sxs-lookup"><span data-stu-id="ddbee-104">EM\_REPLACESEL message</span></span>

<span data-ttu-id="ddbee-105">Substitui o texto selecionado em um controle de edição ou um controle de edição rico pelo texto especificado.</span><span class="sxs-lookup"><span data-stu-id="ddbee-105">Replaces the selected text in an edit control or a rich edit control with the specified text.</span></span>

## <a name="parameters"></a><span data-ttu-id="ddbee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddbee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddbee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ddbee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbee-108">Especifica se a operação de substituição pode ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="ddbee-108">Specifies whether the replacement operation can be undone.</span></span> <span data-ttu-id="ddbee-109">Se isso for **verdadeiro**, a operação poderá ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="ddbee-109">If this is **TRUE**, the operation can be undone.</span></span> <span data-ttu-id="ddbee-110">Se for **false** , a operação não poderá ser desfeita.</span><span class="sxs-lookup"><span data-stu-id="ddbee-110">If this is **FALSE** , the operation cannot be undone.</span></span>

</dd> <dt>

<span data-ttu-id="ddbee-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ddbee-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbee-112">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto de substituição.</span><span class="sxs-lookup"><span data-stu-id="ddbee-112">A pointer to a null-terminated string containing the replacement text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddbee-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ddbee-113">Return value</span></span>

<span data-ttu-id="ddbee-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ddbee-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddbee-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddbee-115">Remarks</span></span>

<span data-ttu-id="ddbee-116">Use a mensagem em **\_ REPLACESEL** para substituir apenas uma parte do texto em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="ddbee-116">Use the **EM\_REPLACESEL** message to replace only a portion of the text in an edit control.</span></span> <span data-ttu-id="ddbee-117">Para substituir todo o texto, use a mensagem [**\_ SetText do WM**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="ddbee-117">To replace all of the text, use the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span>

<span data-ttu-id="ddbee-118">Se não houver seleção, o texto de substituição será inserido no cursor.</span><span class="sxs-lookup"><span data-stu-id="ddbee-118">If there is no selection, the replacement text is inserted at the caret.</span></span>

<span data-ttu-id="ddbee-119">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ddbee-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ddbee-120">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ddbee-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="ddbee-121">Em um controle rich edit, o texto de substituição usa a formatação do caractere no cursor ou, se houver uma seleção, do primeiro caractere na seleção.</span><span class="sxs-lookup"><span data-stu-id="ddbee-121">In a rich edit control, the replacement text takes the formatting of the character at the caret or, if there is a selection, of the first character in the selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbee-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddbee-122">Requirements</span></span>



| <span data-ttu-id="ddbee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddbee-123">Requirement</span></span> | <span data-ttu-id="ddbee-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ddbee-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbee-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddbee-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbee-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ddbee-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ddbee-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ddbee-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbee-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ddbee-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ddbee-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddbee-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddbee-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ddbee-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddbee-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddbee-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbee-132">**SetText do WM \_**</span><span class="sxs-lookup"><span data-stu-id="ddbee-132">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

