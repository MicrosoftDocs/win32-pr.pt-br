---
title: Mensagem de EM_STREAMOUT (RichEdit. h)
description: Faz com que um controle de edição rico passe seu conteúdo para uma função de retorno de chamada EditStreamCallback do aplicativo \ 8211; definida. A função de retorno de chamada pode gravar o fluxo de dados em um arquivo ou em qualquer outro local escolhido por ele.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Controles de EM_STREAMOUT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918490"
---
# <a name="em_streamout-message"></a><span data-ttu-id="bd278-105">Mensagem em fluxo em em \_</span><span class="sxs-lookup"><span data-stu-id="bd278-105">EM\_STREAMOUT message</span></span>

<span data-ttu-id="bd278-106">Faz com que um controle de edição rico passe seu conteúdo para uma função de retorno de chamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd278-106">Causes a rich edit control to pass its contents to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span> <span data-ttu-id="bd278-107">A função de retorno de chamada pode gravar o fluxo de dados em um arquivo ou em qualquer outro local escolhido por ele.</span><span class="sxs-lookup"><span data-stu-id="bd278-107">The callback function can then write the stream of data to a file or any other location that it chooses.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd278-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd278-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd278-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd278-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd278-110">Especifica o formato de dados e as opções de substituição.</span><span class="sxs-lookup"><span data-stu-id="bd278-110">Specifies the data format and replacement options.</span></span>

<span data-ttu-id="bd278-111">Esse valor deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd278-111">This value must be one of the following values.</span></span>



| <span data-ttu-id="bd278-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bd278-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="bd278-113">Significado</span><span class="sxs-lookup"><span data-stu-id="bd278-113">Meaning</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="bd278-114"><dt>**It \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-114"><dt>**SF\_RTF**</dt></span></span> </dl>                   | <span data-ttu-id="bd278-115">RTF.</span><span class="sxs-lookup"><span data-stu-id="bd278-115">RTF.</span></span><br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <span data-ttu-id="bd278-116"><dt>**\_RTFNOOBJS**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-116"><dt>**SF\_RTFNOOBJS**</dt></span></span> </dl> | <span data-ttu-id="bd278-117">RTF com espaços no lugar de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="bd278-117">RTF with spaces in place of COM objects.</span></span><br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="bd278-118"><dt>**texto de it \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-118"><dt>**SF\_TEXT**</dt></span></span> </dl>                | <span data-ttu-id="bd278-119">Texto com espaços no lugar de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="bd278-119">Text with spaces in place of COM objects.</span></span><br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <span data-ttu-id="bd278-120"><dt>**em \_ texto**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-120"><dt>**SF\_TEXTIZED**</dt></span></span> </dl>    | <span data-ttu-id="bd278-121">Texto com uma representação de texto de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="bd278-121">Text with a text representation of COM objects.</span></span><br/> |



 

<span data-ttu-id="bd278-122">A opção **it \_ RTFNOOBJS** é útil se um aplicativo armazena objetos com em si, pois a representação RTF de objetos com não é muito compacta.</span><span class="sxs-lookup"><span data-stu-id="bd278-122">The **SF\_RTFNOOBJS** option is useful if an application stores COM objects itself, as RTF representation of COM objects is not very compact.</span></span> <span data-ttu-id="bd278-123">A palavra de controle, \\ objattph, seguida por um espaço denota a posição do objeto.</span><span class="sxs-lookup"><span data-stu-id="bd278-123">The control word, \\objattph, followed by a space denotes the object position.</span></span>

<span data-ttu-id="bd278-124">Além disso, você pode especificar os sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd278-124">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="bd278-125">Valor</span><span class="sxs-lookup"><span data-stu-id="bd278-125">Value</span></span>                                                                                                                                                            | <span data-ttu-id="bd278-126">Significado</span><span class="sxs-lookup"><span data-stu-id="bd278-126">Meaning</span></span>                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="bd278-127"><dt>**\_PLAINRTF SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-127"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>       | <span data-ttu-id="bd278-128">Se especificado, o controle de edição rico transmite apenas as palavras-chave comuns a todos os idiomas, ignorando palavras-chave específicas de idioma.</span><span class="sxs-lookup"><span data-stu-id="bd278-128">If specified, the rich edit control streams out only the keywords common to all languages, ignoring language-specific keywords.</span></span> <span data-ttu-id="bd278-129">Se não for especificado, o controle rich edit transmitirá todas as palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="bd278-129">If not specified, the rich edit control streams out all keywords.</span></span> <span data-ttu-id="bd278-130">Você pode combinar esse sinalizador com o sinalizador **it \_ RTF** ou **it \_ RTFNOOBJS** .</span><span class="sxs-lookup"><span data-stu-id="bd278-130">You can combine this flag with the **SF\_RTF** or **SF\_RTFNOOBJS** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="bd278-131"><dt>**seleção de SFF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-131"><dt>**SFF\_SELECTION**</dt></span></span> </dl>    | <span data-ttu-id="bd278-132">Se especificado, o controle rich edit transmitirá apenas o conteúdo da seleção atual.</span><span class="sxs-lookup"><span data-stu-id="bd278-132">If specified, the rich edit control streams out only the contents of the current selection.</span></span> <span data-ttu-id="bd278-133">Se não for especificado, o controle transmitirá todo o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bd278-133">If not specified, the control streams out the entire contents.</span></span> <span data-ttu-id="bd278-134">Você pode combinar esse sinalizador com qualquer um dos valores de formato de dados.</span><span class="sxs-lookup"><span data-stu-id="bd278-134">You can combine this flag with any of data format values.</span></span><br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="bd278-135"><dt>**\_Unicode it**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-135"><dt>**SF\_UNICODE**</dt></span></span> </dl>             | <span data-ttu-id="bd278-136">**Microsoft Rich Edit 2,0 e posterior:** Indica texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="bd278-136">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="bd278-137">Você pode combinar esse sinalizador com o sinalizador de **\_ texto it** .</span><span class="sxs-lookup"><span data-stu-id="bd278-137">You can combine this flag with the **SF\_TEXT** flag.</span></span><br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <span data-ttu-id="bd278-138"><dt>**It \_ USECODEPAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-138"><dt>**SF\_USECODEPAGE**</dt></span></span> </dl> | <span data-ttu-id="bd278-139">**Edição avançada 3,0 e posterior:** Gera UTF-8 RTF, bem como texto usando outras páginas de código.</span><span class="sxs-lookup"><span data-stu-id="bd278-139">**Rich Edit 3.0 and later:** Generates UTF-8 RTF as well as text using other code pages.</span></span> <span data-ttu-id="bd278-140">A página de código é definida na palavra alta do *wParam*.</span><span class="sxs-lookup"><span data-stu-id="bd278-140">The code page is set in the high word of *wParam*.</span></span> <span data-ttu-id="bd278-141">Por exemplo, para UTF-8 RTF, defina *wParam* como (CP \_ UTF8 << 16) \| it \_ USECODEPAGE \| it \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="bd278-141">For example, for UTF-8 RTF, set *wParam* to (CP\_UTF8 << 16) \| SF\_USECODEPAGE \| SF\_RTF.</span></span><br/>                               |



 

</dd> <dt>

<span data-ttu-id="bd278-142">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd278-142">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd278-143">Ponteiro para uma estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="bd278-143">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="bd278-144">Na entrada, o membro **pfnCallback** dessa estrutura deve apontar para uma função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd278-144">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="bd278-145">Na saída, o membro **dwError** poderá conter um código de erro diferente de zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="bd278-145">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd278-146">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd278-146">Return value</span></span>

<span data-ttu-id="bd278-147">Essa mensagem retorna o número de caracteres gravados no fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="bd278-147">This message returns the number of characters written to the data stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd278-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd278-148">Remarks</span></span>

<span data-ttu-id="bd278-149">Quando você envia uma mensagem em **\_ StreamOut** , o controle de edição rico faz chamadas repetidas para a função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada pelo membro **pfnCallback** da estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="bd278-149">When you send an **EM\_STREAMOUT** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="bd278-150">Cada vez que ele chama a função de retorno de chamada, o controle passa um buffer contendo uma parte do conteúdo do controle.</span><span class="sxs-lookup"><span data-stu-id="bd278-150">Each time it calls the callback function, the control passes a buffer containing a portion of the contents of the control.</span></span> <span data-ttu-id="bd278-151">Esse processo continua até que o controle tenha passado todo o seu conteúdo para a função de retorno de chamada ou até que ocorra um erro.</span><span class="sxs-lookup"><span data-stu-id="bd278-151">This process continues until the control has passed all its contents to the callback function, or until an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd278-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd278-152">Requirements</span></span>



| <span data-ttu-id="bd278-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd278-153">Requirement</span></span> | <span data-ttu-id="bd278-154">Valor</span><span class="sxs-lookup"><span data-stu-id="bd278-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd278-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd278-155">Minimum supported client</span></span><br/> | <span data-ttu-id="bd278-156">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd278-156">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd278-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd278-157">Minimum supported server</span></span><br/> | <span data-ttu-id="bd278-158">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd278-158">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd278-159">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd278-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd278-160"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd278-160"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd278-161">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd278-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="bd278-162">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bd278-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bd278-163">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="bd278-163">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="bd278-164">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="bd278-164">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="bd278-165">**fluxo de em \_**</span><span class="sxs-lookup"><span data-stu-id="bd278-165">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





