---
title: Mensagem de EM_GETWORDBREAKPROC (WinUser. h)
description: Obtém o endereço da função WordWrap atual. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Controles de EM_GETWORDBREAKPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455610"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="c6585-105">\_Mensagem em GETWORDBREAKPROC</span><span class="sxs-lookup"><span data-stu-id="c6585-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="c6585-106">Obtém o endereço da função WordWrap atual.</span><span class="sxs-lookup"><span data-stu-id="c6585-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="c6585-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="c6585-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6585-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6585-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6585-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6585-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6585-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c6585-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c6585-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6585-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6585-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c6585-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6585-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6585-113">Return value</span></span>

<span data-ttu-id="c6585-114">O valor de retorno especifica o endereço da função WordWrap definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c6585-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="c6585-115">O valor de retorno será **nulo** se não existir nenhuma função WordWrap.</span><span class="sxs-lookup"><span data-stu-id="c6585-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6585-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6585-116">Remarks</span></span>

<span data-ttu-id="c6585-117">Uma função WordWrap examina um buffer de texto que contém o texto a ser enviado para a exibição, procurando a primeira palavra que não caiba na linha de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="c6585-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="c6585-118">A função WordWrap coloca essa palavra no início da próxima linha na exibição.</span><span class="sxs-lookup"><span data-stu-id="c6585-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="c6585-119">Uma função WordWrap define o ponto no qual o sistema deve quebrar uma linha de texto para controles de edição de várias linhas, geralmente com um caractere de espaço que separa duas palavras.</span><span class="sxs-lookup"><span data-stu-id="c6585-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="c6585-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="c6585-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c6585-121">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c6585-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6585-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6585-122">Requirements</span></span>



| <span data-ttu-id="c6585-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6585-123">Requirement</span></span> | <span data-ttu-id="c6585-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c6585-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6585-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6585-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c6585-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6585-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6585-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6585-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c6585-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c6585-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6585-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6585-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6585-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6585-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6585-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6585-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6585-132">**Referência**</span><span class="sxs-lookup"><span data-stu-id="c6585-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6585-133">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="c6585-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="c6585-134">**em \_ FMTLINES**</span><span class="sxs-lookup"><span data-stu-id="c6585-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="c6585-135">**em \_ SETWORDBREAKPROC**</span><span class="sxs-lookup"><span data-stu-id="c6585-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 

