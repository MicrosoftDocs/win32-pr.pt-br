---
title: Mensagem de EM_SETWORDBREAKPROC (WinUser. h)
description: Substitui uma função WordWrap padrão do controle de edição por uma função WordWrap definida pelo aplicativo. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Controles de EM_SETWORDBREAKPROC de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499440"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="e2be3-105">\_Mensagem em SETWORDBREAKPROC</span><span class="sxs-lookup"><span data-stu-id="e2be3-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="e2be3-106">Substitui uma função WordWrap padrão do controle de edição por uma função WordWrap definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2be3-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="e2be3-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="e2be3-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2be3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2be3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2be3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2be3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2be3-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="e2be3-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="e2be3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2be3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2be3-112">O endereço da função WordWrap definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e2be3-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="e2be3-113">Para obter mais informações sobre linhas de quebra, consulte a descrição da função de retorno de chamada [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="e2be3-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2be3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2be3-114">Return value</span></span>

<span data-ttu-id="e2be3-115">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e2be3-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2be3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2be3-116">Remarks</span></span>

<span data-ttu-id="e2be3-117">Uma função WordWrap examina um buffer de texto que contém o texto a ser enviado para a tela, procurando a primeira palavra que não caiba na linha da tela atual.</span><span class="sxs-lookup"><span data-stu-id="e2be3-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="e2be3-118">A função WordWrap coloca essa palavra no início da próxima linha na tela.</span><span class="sxs-lookup"><span data-stu-id="e2be3-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="e2be3-119">Uma função WordWrap define o ponto no qual o sistema deve quebrar uma linha de texto para controles de edição de várias linhas, geralmente com um caractere de espaço que separa duas palavras.</span><span class="sxs-lookup"><span data-stu-id="e2be3-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="e2be3-120">Um controle de várias linhas ou de edição de linha única pode chamar essa função quando o usuário pressiona as teclas de seta em combinação com a tecla CTRL para mover o cursor para a próxima palavra ou palavra anterior.</span><span class="sxs-lookup"><span data-stu-id="e2be3-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="e2be3-121">A função WordWrap padrão quebra uma linha de texto com um caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="e2be3-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="e2be3-122">A função definida pelo aplicativo pode definir o WordWrap para ocorrer em um hífen ou um caractere que não seja o caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="e2be3-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="e2be3-123">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="e2be3-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="e2be3-124">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="e2be3-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e2be3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2be3-125">Requirements</span></span>



| <span data-ttu-id="e2be3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2be3-126">Requirement</span></span> | <span data-ttu-id="e2be3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e2be3-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2be3-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2be3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e2be3-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2be3-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2be3-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2be3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e2be3-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e2be3-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2be3-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2be3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2be3-133"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2be3-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2be3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2be3-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="e2be3-135">**Referência**</span><span class="sxs-lookup"><span data-stu-id="e2be3-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e2be3-136">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="e2be3-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="e2be3-137">**em \_ FMTLINES**</span><span class="sxs-lookup"><span data-stu-id="e2be3-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="e2be3-138">**em \_ GETWORDBREAKPROC**</span><span class="sxs-lookup"><span data-stu-id="e2be3-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 

