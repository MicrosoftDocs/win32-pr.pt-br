---
title: Mensagem de EM_GETSEL (WinUser. h)
description: Obtém as posições de caractere inicial e final (em TCHARs) da seleção atual em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: cf12aaea-cfa7-4804-ae34-fd0992332288
keywords:
- Controles de EM_GETSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28ba97c9043866c3e97c1c51389447498562455
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009308"
---
# <a name="em_getsel-message"></a><span data-ttu-id="12329-105">\_Mensagem em GETSEL</span><span class="sxs-lookup"><span data-stu-id="12329-105">EM\_GETSEL message</span></span>

<span data-ttu-id="12329-106">Obtém as posições de caractere inicial e final (em **TCHAR** s) da seleção atual em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="12329-106">Gets the starting and ending character positions (in **TCHAR** s) of the current selection in an edit control.</span></span> <span data-ttu-id="12329-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="12329-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="12329-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12329-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12329-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="12329-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12329-110">Um ponteiro para um valor **DWORD** que recebe a posição inicial da seleção.</span><span class="sxs-lookup"><span data-stu-id="12329-110">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="12329-111">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="12329-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="12329-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12329-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12329-113">Um ponteiro para um valor **DWORD** que recebe a posição do primeiro caractere não selecionado após o final da seleção.</span><span class="sxs-lookup"><span data-stu-id="12329-113">A pointer to a **DWORD** value that receives the position of the first unselected character after the end of the selection.</span></span> <span data-ttu-id="12329-114">Este parâmetro pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="12329-114">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12329-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12329-115">Return value</span></span>

<span data-ttu-id="12329-116">O valor de retorno é um valor de base zero com a posição inicial da seleção no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e a posição do primeiro **TCHAR** após o último **TCHAR** selecionado no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12329-116">The return value is a zero-based value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and the position of the first **TCHAR** after the last selected **TCHAR** in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="12329-117">Se um desses valores exceder 65.535, o valor de retorno será-1.</span><span class="sxs-lookup"><span data-stu-id="12329-117">If either of these values exceeds 65,535, the return value is -1.</span></span>

<span data-ttu-id="12329-118">É melhor usar os valores retornados em *wParam* e *lParam* porque eles são valores completos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="12329-118">It is better to use the values returned in *wParam* and *lParam* because they are full 32-bit values.</span></span>

## <a name="remarks"></a><span data-ttu-id="12329-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="12329-119">Remarks</span></span>

<span data-ttu-id="12329-120">Se não houver seleção, os valores inicial e final serão a posição do cursor.</span><span class="sxs-lookup"><span data-stu-id="12329-120">If there is no selection, the starting and ending values are both the position of the caret.</span></span>

<span data-ttu-id="12329-121">**Controles de edição avançados:** Você também pode usar a mensagem em [**\_ EXGETSEL**](em-exgetsel.md) para recuperar as mesmas informações.</span><span class="sxs-lookup"><span data-stu-id="12329-121">**Rich edit controls:** You can also use the [**EM\_EXGETSEL**](em-exgetsel.md) message to retrieve the same information.</span></span> <span data-ttu-id="12329-122">**Em \_ EXGETSEL** também retorna posições de caractere inicial e final como valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="12329-122">**EM\_EXGETSEL** also returns starting and ending character positions as 32-bit values.</span></span>

<span data-ttu-id="12329-123">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="12329-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="12329-124">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="12329-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12329-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12329-125">Requirements</span></span>



| <span data-ttu-id="12329-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="12329-126">Requirement</span></span> | <span data-ttu-id="12329-127">Valor</span><span class="sxs-lookup"><span data-stu-id="12329-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12329-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12329-128">Minimum supported client</span></span><br/> | <span data-ttu-id="12329-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12329-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12329-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12329-130">Minimum supported server</span></span><br/> | <span data-ttu-id="12329-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12329-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12329-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12329-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="12329-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12329-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12329-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="12329-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="12329-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="12329-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="12329-136">**em \_ EXGETSEL**</span><span class="sxs-lookup"><span data-stu-id="12329-136">**EM\_EXGETSEL**</span></span>](em-exgetsel.md)
</dt> <dt>

[<span data-ttu-id="12329-137">**em \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="12329-137">**EM\_SETSEL**</span></span>](em-setsel.md)
</dt> </dl>

 

