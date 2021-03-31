---
title: Mensagem de EM_GETEDITSTYLEEX (RichEdit. h)
description: Recupera os sinalizadores de estilo de edição estendida atuais.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- Controles de EM_GETEDITSTYLEEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824464"
---
# <a name="em_geteditstyleex-message"></a><span data-ttu-id="4d2b6-104">\_Mensagem em GETEDITSTYLEEX</span><span class="sxs-lookup"><span data-stu-id="4d2b6-104">EM\_GETEDITSTYLEEX message</span></span>

<span data-ttu-id="4d2b6-105">Recupera os sinalizadores de estilo de edição estendida atuais.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-105">Retrieves the current extended edit style flags.</span></span>


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a><span data-ttu-id="4d2b6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d2b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d2b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4d2b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d2b6-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4d2b6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4d2b6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4d2b6-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d2b6-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4d2b6-111">Return value</span></span>

<span data-ttu-id="4d2b6-112">Retorna os sinalizadores de estilo de edição estendida, que podem incluir um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-112">Returns the extended edit style flags, which can include one or more of the following values.</span></span>



| <span data-ttu-id="4d2b6-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4d2b6-113">Return code</span></span>                                                                                                | <span data-ttu-id="4d2b6-114">Description</span><span class="sxs-lookup"><span data-stu-id="4d2b6-114">Description</span></span>                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4d2b6-115"><dt>**HANDLEFRIENDLYURL de SES \_ ex \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-115"><dt>**SES\_EX\_HANDLEFRIENDLYURL**</dt></span></span> </dl>  | <span data-ttu-id="4d2b6-116">Exibir links de nome amigável com a mesma cor de texto e sublinhado como links automáticos, desde que a formatação temporária não seja usada ou use a cor automática do texto (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-116">Display friendly name links with the same text color and underlining as automatic links, provided that temporary formatting isn t used or uses text autocolor (default: 0).</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="4d2b6-117"><dt>**multitoque de SES \_ ex \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-117"><dt>**SES\_EX\_MULTITOUCH**</dt></span></span> </dl>         | <span data-ttu-id="4d2b6-118">Habilite o suporte ao toque em rich edit.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-118">Enable touch support in Rich Edit.</span></span> <span data-ttu-id="4d2b6-119">Isso inclui seleção, posicionamento de cursor e invocação de menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-119">This includes selection, caret placement, and context-menu invocation.</span></span> <span data-ttu-id="4d2b6-120">Quando esse sinalizador não é definido, o toque é emulado por comandos do mouse, que não usam as especificidades do modo Touch em conta (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-120">When this flag is not set, touch is emulated by mouse commands, which do not take touch-mode specifics into account (default: 0).</span></span> <br/>      |
| <dl> <span data-ttu-id="4d2b6-121"><dt>**NOACETATESELECTION de SES \_ ex \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-121"><dt>**SES\_EX\_NOACETATESELECTION**</dt></span></span> </dl> | <span data-ttu-id="4d2b6-122">Exibe o texto selecionado usando o texto de seleção clássico do Windows e as cores do plano de fundo em vez da cor acetato de segundo plano (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-122">Display selected text using classic Windows selection text and background colors instead of background acetate color (default: 0).</span></span> <br/>                                                                                                               |
| <dl> <span data-ttu-id="4d2b6-123"><dt>**SES \_ ex \_ nomath**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-123"><dt>**SES\_EX\_NOMATH**</dt></span></span> </dl>             | <span data-ttu-id="4d2b6-124">Desabilite a inserção de zonas matemáticas (padrão: 1).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-124">Disable insertion of math zones (default: 1).</span></span> <span data-ttu-id="4d2b6-125">Para habilitar a edição e a exibição de matemática, envie a mensagem em [**\_ SETEDITSTYLEEX**](em-seteditstyleex.md) com *wParam* definido como 0 e *lParam* definido como **ses \_ ex \_ nomath**.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-125">To enable math editing and display, send the [**EM\_SETEDITSTYLEEX**](em-seteditstyleex.md) message with *wParam* set to 0, and *lParam* set to **SES\_EX\_NOMATH**.</span></span> <br/>                              |
| <dl> <span data-ttu-id="4d2b6-126"><dt>**SES \_ ex \_ notável**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-126"><dt>**SES\_EX\_NOTABLE**</dt></span></span> </dl>            | <span data-ttu-id="4d2b6-127">Desabilite a inserção de tabelas.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-127">Disable insertion of tables.</span></span> <span data-ttu-id="4d2b6-128">A mensagem em [**\_ InsertTable**](em-inserttable.md) retorna e as tabelas de **\_ falha** e RTF são ignoradas (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-128">The [**EM\_INSERTTABLE**](em-inserttable.md) message returns **E\_FAIL** and RTF tables are skipped (default: 0).</span></span> <br/>                                                                                                  |
| <dl> <span data-ttu-id="4d2b6-129"><dt>**USESINGLELINE de SES \_ ex \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-129"><dt>**SES\_EX\_USESINGLELINE**</dt></span></span> </dl>      | <span data-ttu-id="4d2b6-130">Habilite um controle de várias linhas para agir como um controle de linha única com a capacidade de rolar verticalmente quando a altura da linha única for maior que a altura da janela (padrão: 0).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-130">Enable a multiline control to act like a single-line control with the ability to scroll vertically when the single-line height is greater than the window height (default: 0).</span></span> <br/>                                                                   |
| <dl> <span data-ttu-id="4d2b6-131"><dt>**HIDETEMPFORMAT de SES \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-131"><dt>**SES\_HIDETEMPFORMAT**</dt></span></span> </dl>         | <span data-ttu-id="4d2b6-132">Oculte a formatação temporária que é criada quando [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) é chamado com **tomApplyTmp**.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-132">Hide temporary formatting that is created when [**ITextFont.Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) is called with **tomApplyTmp**.</span></span> <span data-ttu-id="4d2b6-133">Por exemplo, essa formatação é usada por verificadores ortográficos para exibir um sublinhado ondulado sob possíveis palavras escritas incorretamente.</span><span class="sxs-lookup"><span data-stu-id="4d2b6-133">For example, such formatting is used by spell checkers to display a squiggly underline under possibly misspelled words.</span></span><br/> |
| <dl> <span data-ttu-id="4d2b6-134"><dt>**USEMOUSEWPARAM de SES \_ ex \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-134"><dt>**SES\_EX\_USEMOUSEWPARAM**</dt></span></span> </dl>     | <span data-ttu-id="4d2b6-135">Use *wParam* ao manipular a [**mensagem \_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) e não chame [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="4d2b6-135">Use *wParam* when handling the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message and do not call [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="4d2b6-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d2b6-136">Requirements</span></span>



| <span data-ttu-id="4d2b6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d2b6-137">Requirement</span></span> | <span data-ttu-id="4d2b6-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4d2b6-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2b6-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d2b6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2b6-140">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4d2b6-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4d2b6-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d2b6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2b6-142">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4d2b6-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4d2b6-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d2b6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d2b6-144"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d2b6-144"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d2b6-145">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4d2b6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2b6-146">**em \_ SETEDITSTYLEEX**</span><span class="sxs-lookup"><span data-stu-id="4d2b6-146">**EM\_SETEDITSTYLEEX**</span></span>](em-seteditstyleex.md)
</dt> </dl>

 

