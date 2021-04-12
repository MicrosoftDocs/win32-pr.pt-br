---
title: Mensagem de EM_CHARFROMPOS (WinUser. h)
description: Obtém informações sobre o caractere mais próximo de um ponto especificado na área do cliente de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: fe9f96f2-5b3c-4039-befd-5e9a456ba32d
keywords:
- Controles de EM_CHARFROMPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_CHARFROMPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1156d69c012faa0141726c00ab880d954fe2857
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455443"
---
# <a name="em_charfrompos-message"></a><span data-ttu-id="e5b67-105">\_Mensagem em CHARFROMPOS</span><span class="sxs-lookup"><span data-stu-id="e5b67-105">EM\_CHARFROMPOS message</span></span>

<span data-ttu-id="e5b67-106">Obtém informações sobre o caractere mais próximo de um ponto especificado na área do cliente de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="e5b67-106">Gets information about the character closest to a specified point in the client area of an edit control.</span></span> <span data-ttu-id="e5b67-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="e5b67-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e5b67-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5b67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5b67-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5b67-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b67-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e5b67-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e5b67-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5b67-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5b67-112">As coordenadas de um ponto na área do cliente do controle.</span><span class="sxs-lookup"><span data-stu-id="e5b67-112">The coordinates of a point in the control's client area.</span></span> <span data-ttu-id="e5b67-113">As coordenadas estão em unidades de tela e são relativas ao canto superior esquerdo da área do cliente do controle.</span><span class="sxs-lookup"><span data-stu-id="e5b67-113">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="e5b67-114">**Controles de edição avançados:** Um ponteiro para uma estrutura [**pontual**](/previous-versions//dd162807(v=vs.85)) que contém as coordenadas horizontais e verticais.</span><span class="sxs-lookup"><span data-stu-id="e5b67-114">**Rich edit controls:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that contains the horizontal and vertical coordinates.</span></span>

<span data-ttu-id="e5b67-115">**Controles de edição:** O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém a coordenada horizontal.</span><span class="sxs-lookup"><span data-stu-id="e5b67-115">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate.</span></span> <span data-ttu-id="e5b67-116">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém a coordenada vertical.</span><span class="sxs-lookup"><span data-stu-id="e5b67-116">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5b67-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5b67-117">Return value</span></span>

<span data-ttu-id="e5b67-118">**Controles de edição avançados:** O valor de retorno especifica o índice de caracteres com base em zero do caractere mais próximo ao ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="e5b67-118">**Rich edit controls:** The return value specifies the zero-based character index of the character nearest the specified point.</span></span> <span data-ttu-id="e5b67-119">O valor de retorno indica o último caractere no controle de edição se o ponto especificado estiver além do último caractere no controle.</span><span class="sxs-lookup"><span data-stu-id="e5b67-119">The return value indicates the last character in the edit control if the specified point is beyond the last character in the control.</span></span>

<span data-ttu-id="e5b67-120">**Controles de edição:** O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice de base zero do caractere mais próximo ao ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="e5b67-120">**Edit controls:** The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the character nearest the specified point.</span></span> <span data-ttu-id="e5b67-121">Esse índice é relativo ao início do controle, não ao início da linha.</span><span class="sxs-lookup"><span data-stu-id="e5b67-121">This index is relative to the beginning of the control, not the beginning of the line.</span></span> <span data-ttu-id="e5b67-122">Se o ponto especificado estiver além do último caractere no controle de edição, o valor de retorno indicará o último caractere no controle.</span><span class="sxs-lookup"><span data-stu-id="e5b67-122">If the specified point is beyond the last character in the edit control, the return value indicates the last character in the control.</span></span> <span data-ttu-id="e5b67-123">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o índice de base zero da linha que contém o caractere.</span><span class="sxs-lookup"><span data-stu-id="e5b67-123">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the line that contains the character.</span></span> <span data-ttu-id="e5b67-124">Para controles de edição de linha única, esse valor é zero.</span><span class="sxs-lookup"><span data-stu-id="e5b67-124">For single-line edit controls, this value is zero.</span></span> <span data-ttu-id="e5b67-125">O índice indica o delimitador de linha se o ponto especificado estiver além do último caractere visível em uma linha.</span><span class="sxs-lookup"><span data-stu-id="e5b67-125">The index indicates the line delimiter if the specified point is beyond the last visible character in a line.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5b67-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5b67-126">Remarks</span></span>

<span data-ttu-id="e5b67-127">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="e5b67-127">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e5b67-128">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e5b67-128">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

<span data-ttu-id="e5b67-129">Se um ponto for passado para **em \_ CHARFROMPOS** como o *lParam* e o ponto estiver fora dos limites do controle de edição, o *LRESULT* será (65535, 65535).</span><span class="sxs-lookup"><span data-stu-id="e5b67-129">If a point is passed to **EM\_CHARFROMPOS** as the *lParam* and the point is outside the bounds of the edit control, then the *lResult* is (65535, 65535).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5b67-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5b67-130">Requirements</span></span>



| <span data-ttu-id="e5b67-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5b67-131">Requirement</span></span> | <span data-ttu-id="e5b67-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e5b67-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5b67-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b67-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e5b67-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5b67-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e5b67-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5b67-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e5b67-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e5b67-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5b67-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5b67-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5b67-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5b67-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5b67-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5b67-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5b67-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e5b67-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5b67-141">**em \_ POSFROMCHAR**</span><span class="sxs-lookup"><span data-stu-id="e5b67-141">**EM\_POSFROMCHAR**</span></span>](em-posfromchar.md)
</dt> <dt>

<span data-ttu-id="e5b67-142">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="e5b67-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="e5b67-143">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="e5b67-143">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> <dt>

<span data-ttu-id="e5b67-144">[**PONTO**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e5b67-144">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

