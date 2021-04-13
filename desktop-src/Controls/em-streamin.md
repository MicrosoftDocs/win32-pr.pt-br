---
title: Mensagem de EM_STREAMIN (RichEdit. h)
description: Substitui o conteúdo de um controle de edição rico por um fluxo de dados fornecidos por um aplicativo definido \ 8211; Função de retorno de chamada EditStreamCallback.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Controles de EM_STREAMIN de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455666"
---
# <a name="em_streamin-message"></a><span data-ttu-id="7dd77-104">Mensagem de fluxo em em \_</span><span class="sxs-lookup"><span data-stu-id="7dd77-104">EM\_STREAMIN message</span></span>

<span data-ttu-id="7dd77-105">Substitui o conteúdo de um controle de edição rico por um fluxo de dados fornecidos por uma função de retorno de chamada [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dd77-105">Replaces the contents of a rich edit control with a stream of data provided by an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) callback function.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dd77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dd77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7dd77-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dd77-108">Especifica o formato de dados e as opções de substituição.</span><span class="sxs-lookup"><span data-stu-id="7dd77-108">Specifies the data format and replacement options.</span></span> <span data-ttu-id="7dd77-109">Esse valor deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7dd77-109">This value must be one of the following values.</span></span>



| <span data-ttu-id="7dd77-110">Valor</span><span class="sxs-lookup"><span data-stu-id="7dd77-110">Value</span></span>                                                                                                                                       | <span data-ttu-id="7dd77-111">Significado</span><span class="sxs-lookup"><span data-stu-id="7dd77-111">Meaning</span></span>         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <span data-ttu-id="7dd77-112"><dt>**It \_ RTF**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd77-112"><dt>**SF\_RTF**</dt></span></span> </dl>    | <span data-ttu-id="7dd77-113">RTF</span><span class="sxs-lookup"><span data-stu-id="7dd77-113">RTF</span></span><br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <span data-ttu-id="7dd77-114"><dt>**texto de it \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd77-114"><dt>**SF\_TEXT**</dt></span></span> </dl> | <span data-ttu-id="7dd77-115">Texto</span><span class="sxs-lookup"><span data-stu-id="7dd77-115">Text</span></span><br/> |



 

<span data-ttu-id="7dd77-116">Além disso, você pode especificar os sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7dd77-116">In addition, you can specify the following flags.</span></span>



| <span data-ttu-id="7dd77-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7dd77-117">Value</span></span>                                                                                                                                                         | <span data-ttu-id="7dd77-118">Significado</span><span class="sxs-lookup"><span data-stu-id="7dd77-118">Meaning</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <span data-ttu-id="7dd77-119"><dt>**\_PLAINRTF SFF**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd77-119"><dt>**SFF\_PLAINRTF**</dt></span></span> </dl>    | <span data-ttu-id="7dd77-120">Se especificado, somente palavras-chave comuns a todos os idiomas serão transmitidas em fluxo.</span><span class="sxs-lookup"><span data-stu-id="7dd77-120">If specified, only keywords common to all languages are streamed in.</span></span> <span data-ttu-id="7dd77-121">Palavras-chave RTF específicas do idioma no fluxo são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="7dd77-121">Language-specific RTF keywords in the stream are ignored.</span></span> <span data-ttu-id="7dd77-122">Se não for especificado, todas as palavras-chave serão transmitidas.</span><span class="sxs-lookup"><span data-stu-id="7dd77-122">If not specified, all keywords are streamed in.</span></span> <span data-ttu-id="7dd77-123">Você pode combinar esse sinalizador com o sinalizador **it \_ RTF** .</span><span class="sxs-lookup"><span data-stu-id="7dd77-123">You can combine this flag with the **SF\_RTF** flag.</span></span><br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <span data-ttu-id="7dd77-124"><dt>**seleção de SFF \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd77-124"><dt>**SFF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="7dd77-125">Se especificado, o fluxo de dados substituirá o conteúdo da seleção atual.</span><span class="sxs-lookup"><span data-stu-id="7dd77-125">If specified, the data stream replaces the contents of the current selection.</span></span> <span data-ttu-id="7dd77-126">Se não for especificado, o fluxo de dados substituirá todo o conteúdo do controle.</span><span class="sxs-lookup"><span data-stu-id="7dd77-126">If not specified, the data stream replaces the entire contents of the control.</span></span> <span data-ttu-id="7dd77-127">Você pode combinar esse sinalizador com os sinalizadores de **\_ texto** de it ou **it \_ RTF** .</span><span class="sxs-lookup"><span data-stu-id="7dd77-127">You can combine this flag with the **SF\_TEXT** or **SF\_RTF** flags.</span></span><br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <span data-ttu-id="7dd77-128"><dt>**\_Unicode it**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd77-128"><dt>**SF\_UNICODE**</dt></span></span> </dl>          | <span data-ttu-id="7dd77-129">**Microsoft Rich Edit 2,0 e posterior:** Indica texto Unicode.</span><span class="sxs-lookup"><span data-stu-id="7dd77-129">**Microsoft Rich Edit 2.0 and later:** Indicates Unicode text.</span></span> <span data-ttu-id="7dd77-130">Você pode combinar esse sinalizador com o sinalizador de **\_ texto it** .</span><span class="sxs-lookup"><span data-stu-id="7dd77-130">You can combine this flag with the **SF\_TEXT** flag.</span></span> <br/>                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="7dd77-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dd77-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dd77-132">Ponteiro para uma estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="7dd77-132">Pointer to an [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="7dd77-133">Na entrada, o membro **pfnCallback** dessa estrutura deve apontar para uma função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7dd77-133">On input, the **pfnCallback** member of this structure must point to an application defined [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function.</span></span> <span data-ttu-id="7dd77-134">Na saída, o membro **dwError** poderá conter um código de erro diferente de zero se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="7dd77-134">On output, the **dwError** member can contain a nonzero error code if an error occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd77-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7dd77-135">Return value</span></span>

<span data-ttu-id="7dd77-136">Essa mensagem retorna o número de caracteres lidos.</span><span class="sxs-lookup"><span data-stu-id="7dd77-136">This message returns the number of characters read.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd77-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dd77-137">Remarks</span></span>

<span data-ttu-id="7dd77-138">Quando você envia uma mensagem de **\_ fluxo** em em, o controle de edição rico faz chamadas repetidas para a função [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) especificada pelo membro **pfnCallback** da estrutura [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) .</span><span class="sxs-lookup"><span data-stu-id="7dd77-138">When you send an **EM\_STREAMIN** message, the rich edit control makes repeated calls to the [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) function specified by the **pfnCallback** member of the [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream) structure.</span></span> <span data-ttu-id="7dd77-139">Cada vez que a função de retorno de chamada é chamada, ela preenche um buffer com dados para ler no controle.</span><span class="sxs-lookup"><span data-stu-id="7dd77-139">Each time the callback function is called, it fills a buffer with data to read into the control.</span></span> <span data-ttu-id="7dd77-140">Isso continuará até que a função de retorno de chamada indique que a operação de entrada de fluxo foi concluída ou ocorrerá um erro.</span><span class="sxs-lookup"><span data-stu-id="7dd77-140">This continues until the callback function indicates that the stream-in operation has been completed or an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dd77-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dd77-141">Requirements</span></span>



| <span data-ttu-id="7dd77-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dd77-142">Requirement</span></span> | <span data-ttu-id="7dd77-143">Valor</span><span class="sxs-lookup"><span data-stu-id="7dd77-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd77-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dd77-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd77-145">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dd77-145">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7dd77-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dd77-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd77-147">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7dd77-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7dd77-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dd77-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd77-149"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd77-149"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd77-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dd77-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="7dd77-151">**Referência**</span><span class="sxs-lookup"><span data-stu-id="7dd77-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7dd77-152">**EDITSTREAM**</span><span class="sxs-lookup"><span data-stu-id="7dd77-152">**EDITSTREAM**</span></span>](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[<span data-ttu-id="7dd77-153">*EditStreamCallback*</span><span class="sxs-lookup"><span data-stu-id="7dd77-153">*EditStreamCallback*</span></span>](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[<span data-ttu-id="7dd77-154">**em \_ fluxo contínuo**</span><span class="sxs-lookup"><span data-stu-id="7dd77-154">**EM\_STREAMOUT**</span></span>](em-streamout.md)
</dt> </dl>

 

 





