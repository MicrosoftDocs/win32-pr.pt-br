---
title: Mensagem de EM_AUTOURLDETECT (RichEdit. h)
description: Habilita ou desabilita a detecção automática de hiperlinks por um controle de edição rico.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Controles de EM_AUTOURLDETECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918711"
---
# <a name="em_autourldetect-message"></a><span data-ttu-id="fec82-104">\_Mensagem em AUTOURLDETECT</span><span class="sxs-lookup"><span data-stu-id="fec82-104">EM\_AUTOURLDETECT message</span></span>

<span data-ttu-id="fec82-105">Habilita ou desabilita a detecção automática de hiperlinks por um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="fec82-105">Enables or disables automatic detection of hyperlinks by a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fec82-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fec82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fec82-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fec82-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fec82-108">Especifique 0 para desabilitar a detecção automática de link ou um dos valores a seguir para habilitar vários tipos de detecção.</span><span class="sxs-lookup"><span data-stu-id="fec82-108">Specify 0 to disable automatic link detection, or one of the following values to enable various kinds of detection.</span></span>



| <span data-ttu-id="fec82-109">Valor</span><span class="sxs-lookup"><span data-stu-id="fec82-109">Value</span></span>                                                                                                                                                                                       | <span data-ttu-id="fec82-110">Significado</span><span class="sxs-lookup"><span data-stu-id="fec82-110">Meaning</span></span>                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <span data-ttu-id="fec82-111"><dt>**AURL \_ DISABLEMIXEDLGC**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-111"><dt>**AURL\_DISABLEMIXEDLGC**</dt></span></span> </dl>          | <span data-ttu-id="fec82-112">**Windows 8**: desabilite o reconhecimento de nomes de domínio que contêm rótulos com caracteres que pertencem a mais de um dos seguintes scripts: latim, grego e cirílico.</span><span class="sxs-lookup"><span data-stu-id="fec82-112">**Windows 8**: Disable recognition of domain names that contain labels with characters belonging to more than one of the following scripts: Latin, Greek, and Cyrillic.</span></span> <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <span data-ttu-id="fec82-113"><dt>**AURL \_ ENABLEDRIVELETTERS**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-113"><dt>**AURL\_ENABLEDRIVELETTERS**</dt></span></span> </dl> | <span data-ttu-id="fec82-114">**Windows 8**: reconhecer nomes de arquivos que têm uma especificação de unidade principal, como c: \\ Temp.</span><span class="sxs-lookup"><span data-stu-id="fec82-114">**Windows 8**: Recognize file names that have a leading drive specification, such as c:\\temp.</span></span><br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <span data-ttu-id="fec82-115"><dt>**AURL \_ ENABLEEA**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-115"><dt>**AURL\_ENABLEEA**</dt></span></span> </dl>                               | <span data-ttu-id="fec82-116">Esse valor é preterido; em vez disso, use **AURL \_ ENABLEEAURLS** .</span><span class="sxs-lookup"><span data-stu-id="fec82-116">This value is deprecated; use **AURL\_ENABLEEAURLS** instead.</span></span><br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <span data-ttu-id="fec82-117"><dt>**AURL \_ ENABLEEAURLS**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-117"><dt>**AURL\_ENABLEEAURLS**</dt></span></span> </dl>                   | <span data-ttu-id="fec82-118">Reconhecer URLs que contêm caracteres do leste asiático.</span><span class="sxs-lookup"><span data-stu-id="fec82-118">Recognize URLs that contain East Asian characters.</span></span> <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <span data-ttu-id="fec82-119"><dt>**AURL \_ ENABLEEMAILADDR**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-119"><dt>**AURL\_ENABLEEMAILADDR**</dt></span></span> </dl>          | <span data-ttu-id="fec82-120">**Windows 8**: reconhecer endereços de email.</span><span class="sxs-lookup"><span data-stu-id="fec82-120">**Windows 8**: Recognize email addresses.</span></span><br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <span data-ttu-id="fec82-121"><dt>**AURL \_ ENABLETELNO**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-121"><dt>**AURL\_ENABLETELNO**</dt></span></span> </dl>                      | <span data-ttu-id="fec82-122">**Windows 8**: reconhecer números de telefone.</span><span class="sxs-lookup"><span data-stu-id="fec82-122">**Windows 8**: Recognize telephone numbers.</span></span><br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <span data-ttu-id="fec82-123"><dt>**AURL \_ ENABLEURL**</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-123"><dt>**AURL\_ENABLEURL**</dt></span></span> </dl>                            | <span data-ttu-id="fec82-124">**Windows 8**: reconhecer URLs que incluem o caminho.</span><span class="sxs-lookup"><span data-stu-id="fec82-124">**Windows 8**: Recognize URLs that include the path.</span></span><br/>                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="fec82-125">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fec82-125">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fec82-126">Esse parâmetro determinará os esquemas de URL reconhecidos se **AURL \_ ENABLEURL** estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="fec82-126">This parameter determines the URL schemes recognized if **AURL\_ENABLEURL** is active.</span></span> <span data-ttu-id="fec82-127">Se *lParam* for NULL, a lista de nome de esquema padrão será usada (consulte comentários).</span><span class="sxs-lookup"><span data-stu-id="fec82-127">If *lParam* is NULL, the default scheme name list is used (see Remarks).</span></span> <span data-ttu-id="fec82-128">Como alternativa, *lParam* pode apontar para uma cadeia de caracteres terminada em nulo que consiste em até 50 de nomes de esquema terminados por dois-pontos que substituem a lista de nome de esquema padrão.</span><span class="sxs-lookup"><span data-stu-id="fec82-128">Alternatively, *lParam* can point to a null-terminated string consisting of up to 50 colon-terminated scheme names that supersede the default scheme name list.</span></span> <span data-ttu-id="fec82-129">Por exemplo, a cadeia de caracteres poderia ser "News: http: ftp: Telnet:".</span><span class="sxs-lookup"><span data-stu-id="fec82-129">For example, the string could be "news:http:ftp:telnet:".</span></span> <span data-ttu-id="fec82-130">A sintaxe do nome do esquema é definida no [Uniform Resource Identifiers (URI): documento de sintaxe genérica]( https://www.ietf.org/rfc/rfc2396.txt) no site da IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="fec82-130">The scheme name syntax is defined in the [Uniform Resource Identifiers (URI): Generic Syntax]( https://www.ietf.org/rfc/rfc2396.txt) document on The Internet Engineering Task Force (IETF) website.</span></span> <span data-ttu-id="fec82-131">Especificamente, um nome de esquema pode conter até 13 caracteres (incluindo os dois-pontos), deve começar com um alfabeto ASCII e pode ser seguido por uma mistura de alfabetos ASCII, dígitos e os três caracteres de Pontuação: ".", "+" e "-".</span><span class="sxs-lookup"><span data-stu-id="fec82-131">Specifically, a scheme name can contain up to 13 characters (including the colon), must start with an ASCII alphabetic, and can be followed by a mixture of ASCII alphabetics, digits, and the three punctuation characters: ".", "+", and "-".</span></span> <span data-ttu-id="fec82-132">O tipo de cadeia de caracteres pode ser **Char \** _ ou _*WCHAR \*\*_; o controle de edição rico detecta automaticamente o tipo.</span><span class="sxs-lookup"><span data-stu-id="fec82-132">The string type can be either **char\** _ or _*WCHAR\*\*_; the rich edit control automatically detects the type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fec82-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fec82-133">Return value</span></span>

<span data-ttu-id="fec82-134">Se a mensagem tiver sucesso, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="fec82-134">If the message succeeds, the return value is zero.</span></span>

<span data-ttu-id="fec82-135">Se a mensagem falhar, o valor de retorno será um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="fec82-135">If the message fails, the return value is a nonzero value.</span></span> <span data-ttu-id="fec82-136">Por exemplo, a mensagem pode falhar devido a memória insuficiente, uma opção de detecção inválida ou uma cadeia de caracteres de nome de esquema inválida.</span><span class="sxs-lookup"><span data-stu-id="fec82-136">For example, the message might fail due to insufficient memory, an invalid detection option, or an invalid scheme-name string.</span></span>

<span data-ttu-id="fec82-137">Se _lParam \* contiver mais de 50 nomes de esquema, a mensagem falhará com um valor de retorno de **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="fec82-137">If _lParam\* contains more than 50 scheme names, the message fails with a return value of **E\_INVALIDARG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec82-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="fec82-138">Remarks</span></span>

<span data-ttu-id="fec82-139">Se a detecção automática de URL estiver habilitada (ou seja, *wParam* incluir **AURL \_ ENABLEURL**), o controle de edição rico examinará qualquer texto modificado para determinar se o texto corresponde ao formato de uma URL (ou mais geralmente no Windows 8 ou posterior um identificador de recurso internacional IRI).</span><span class="sxs-lookup"><span data-stu-id="fec82-139">If automatic URL detection is enabled (that is, *wParam* includes **AURL\_ENABLEURL**), the rich edit control scans any modified text to determine whether the text matches the format of a URL (or more generally in Windows 8 or later an IRI International Resource Identifier).</span></span> <span data-ttu-id="fec82-140">Se *lParam* for NULL, o controle detectará URLs que começam com os seguintes nomes de esquema:</span><span class="sxs-lookup"><span data-stu-id="fec82-140">If *lParam* is NULL, the control detects URLs that begin with the following scheme names:</span></span>

-   <span data-ttu-id="fec82-141">callto</span><span class="sxs-lookup"><span data-stu-id="fec82-141">callto</span></span>
-   <span data-ttu-id="fec82-142">arquivo</span><span class="sxs-lookup"><span data-stu-id="fec82-142">file</span></span>
-   <span data-ttu-id="fec82-143">FTP</span><span class="sxs-lookup"><span data-stu-id="fec82-143">ftp</span></span>
-   <span data-ttu-id="fec82-144">gopher</span><span class="sxs-lookup"><span data-stu-id="fec82-144">gopher</span></span>
-   <span data-ttu-id="fec82-145">http</span><span class="sxs-lookup"><span data-stu-id="fec82-145">http</span></span>
-   <span data-ttu-id="fec82-146">HTTPS</span><span class="sxs-lookup"><span data-stu-id="fec82-146">https</span></span>
-   <span data-ttu-id="fec82-147">mailto</span><span class="sxs-lookup"><span data-stu-id="fec82-147">mailto</span></span>
-   <span data-ttu-id="fec82-148">notícias</span><span class="sxs-lookup"><span data-stu-id="fec82-148">news</span></span>
-   <span data-ttu-id="fec82-149">HDInsight</span><span class="sxs-lookup"><span data-stu-id="fec82-149">notes</span></span>
-   <span data-ttu-id="fec82-150">NNTP</span><span class="sxs-lookup"><span data-stu-id="fec82-150">nntp</span></span>
-   <span data-ttu-id="fec82-151">onenote</span><span class="sxs-lookup"><span data-stu-id="fec82-151">onenote</span></span>
-   <span data-ttu-id="fec82-152">outlook</span><span class="sxs-lookup"><span data-stu-id="fec82-152">outlook</span></span>
-   <span data-ttu-id="fec82-153">prospero</span><span class="sxs-lookup"><span data-stu-id="fec82-153">prospero</span></span>
-   <span data-ttu-id="fec82-154">tel</span><span class="sxs-lookup"><span data-stu-id="fec82-154">tel</span></span>
-   <span data-ttu-id="fec82-155">telnet</span><span class="sxs-lookup"><span data-stu-id="fec82-155">telnet</span></span>
-   <span data-ttu-id="fec82-156">wais</span><span class="sxs-lookup"><span data-stu-id="fec82-156">wais</span></span>
-   <span data-ttu-id="fec82-157">webcal</span><span class="sxs-lookup"><span data-stu-id="fec82-157">webcal</span></span>

<span data-ttu-id="fec82-158">Quando a detecção automática de link está habilitada, o controle de edição rico remove o efeito de **\_ link CFE** do texto modificado que não tem um formato reconhecido pelo controle.</span><span class="sxs-lookup"><span data-stu-id="fec82-158">When automatic link detection is enabled, the rich edit control removes the **CFE\_LINK** effect from modified text that does not have a format recognized by the control.</span></span> <span data-ttu-id="fec82-159">Se seu aplicativo usar o efeito de **\_ link CFE** para marcar outros tipos de texto, não habilite a detecção automática de link.</span><span class="sxs-lookup"><span data-stu-id="fec82-159">If your application uses the **CFE\_LINK** effect to mark other types of text, do not enable automatic link detection.</span></span> <span data-ttu-id="fec82-160">O controle de edição rico não verifica se existe um link detectado; essa responsabilidade pertence ao cliente.</span><span class="sxs-lookup"><span data-stu-id="fec82-160">The rich edit control does not check whether a detected link exists; that responsibility belongs to the client.</span></span>

<span data-ttu-id="fec82-161">Um controle de edição rico envia a notificação de [ \_ link en](en-link.md) quando recebe várias mensagens enquanto o ponteiro do mouse está sobre o texto que tem o efeito de **\_ link CFE** .</span><span class="sxs-lookup"><span data-stu-id="fec82-161">A rich edit control sends the [EN\_LINK](en-link.md) notification when it receives various messages while the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="fec82-162">Para obter mais informações, consulte hiperlinks [automáticos de RichEdit](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [hiperlinks de nome amigável do RichEdit](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span><span class="sxs-lookup"><span data-stu-id="fec82-162">For more information, see [Automatic RichEdit Hyperlinks](/archive/blogs/murrays/automatic-richedit-hyperlinks) and [RichEdit Friendly Name Hyperlinks](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).</span></span>

## <a name="requirements"></a><span data-ttu-id="fec82-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec82-163">Requirements</span></span>



| <span data-ttu-id="fec82-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec82-164">Requirement</span></span> | <span data-ttu-id="fec82-165">Valor</span><span class="sxs-lookup"><span data-stu-id="fec82-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fec82-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fec82-166">Minimum supported client</span></span><br/> | <span data-ttu-id="fec82-167">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fec82-167">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fec82-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fec82-168">Minimum supported server</span></span><br/> | <span data-ttu-id="fec82-169">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fec82-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fec82-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fec82-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="fec82-171"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="fec82-171"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fec82-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec82-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec82-173">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="fec82-173">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[<span data-ttu-id="fec82-174">\_link para</span><span class="sxs-lookup"><span data-stu-id="fec82-174">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

