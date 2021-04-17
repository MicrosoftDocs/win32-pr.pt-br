---
title: Constantes de estrutura diversas (msctf. h)
description: As constantes de estrutura diversas indicam configurações para clientes, processos ou texto.
ms.assetid: fa53c1f1-50eb-45eb-b2ea-f236a376d41a
topic_type:
- apiref
api_name:
- TF_CLIENTID_NULL
- TF_INVALID_GUIDATOM
- TF_DEFAULT_SELECTION
- TF_GTP_INCL_TEXT
- TF_HF_OBJECT
- TF_IE_CORRECTION
- TF_INVALID_COOKIE
- TF_INVALID_EDIT_COOKIE
- TF_POPF_ALL
- TF_ST_CORRECTION
- TF_TU_CORRECTION
- TF_US_HIDETIPUI
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9eab083f6763d4244d0720b04c2a22744febc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455715"
---
# <a name="miscellaneous-framework-constants"></a><span data-ttu-id="f85fd-103">Constantes de estrutura diversas</span><span class="sxs-lookup"><span data-stu-id="f85fd-103">Miscellaneous Framework Constants</span></span>

<span data-ttu-id="f85fd-104">As constantes de estrutura diversas indicam configurações para clientes, processos ou texto.</span><span class="sxs-lookup"><span data-stu-id="f85fd-104">Miscellaneous framework constants indicate settings for clients, processes, or text.</span></span>



| <span data-ttu-id="f85fd-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="f85fd-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="f85fd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f85fd-106">Description</span></span>                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <span data-ttu-id="f85fd-107"><dt>**TF \_ CLIENTID \_ nulo**</dt> <dt>((TfClientId) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-107"><dt>**TF\_CLIENTID\_NULL**</dt> <dt>((TfClientId)0)</dt></span></span> </dl>                        | <span data-ttu-id="f85fd-108">Indica para um serviço de texto que o cliente é desativado.</span><span class="sxs-lookup"><span data-stu-id="f85fd-108">Indicates to a text service that the client is deactivated.</span></span> <span data-ttu-id="f85fd-109">Consulte [TfClientId](tfclientid.md).</span><span class="sxs-lookup"><span data-stu-id="f85fd-109">See [TfClientId](tfclientid.md).</span></span><br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <span data-ttu-id="f85fd-110"><dt>**TF \_ \_GUIDATOM inválido**</dt> <dt>((TfGuidAtom) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-110"><dt>**TF\_INVALID\_GUIDATOM**</dt> <dt>((TfGuidAtom)0)</dt></span></span> </dl>               | <span data-ttu-id="f85fd-111">O valor de [TfGuidAtom](tfguidatom.md) para o processo atual é inválido.</span><span class="sxs-lookup"><span data-stu-id="f85fd-111">The [TfGuidAtom](tfguidatom.md) value for the current process is invalid.</span></span><br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <span data-ttu-id="f85fd-112"><dt>**TF \_ \_seleção padrão**</dt> <dt>( \_ seleção padrão de TS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-112"><dt>**TF\_DEFAULT\_SELECTION**</dt> <dt>( TS\_DEFAULT\_SELECTION )</dt></span></span> </dl> | <span data-ttu-id="f85fd-113">Use a seleção padrão.</span><span class="sxs-lookup"><span data-stu-id="f85fd-113">Use the default selection.</span></span> <span data-ttu-id="f85fd-114">Usado por [ITfContext:: getseleções](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)e [ITextStoreAnchor:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span><span class="sxs-lookup"><span data-stu-id="f85fd-114">Used by [ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection), and [ITextStoreAnchor::GetSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).</span></span><br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <span data-ttu-id="f85fd-115"><dt>**TF \_ GTP \_ incl \_ Text**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-115"><dt>**TF\_GTP\_INCL\_TEXT**</dt> <dt>( 0x1 )</dt></span></span> </dl>                               | <span data-ttu-id="f85fd-116">Especifica que o método [ITfEditRecord:: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obterá a coleção de objetos Range que abrangem o texto alterado durante a sessão de edição.</span><span class="sxs-lookup"><span data-stu-id="f85fd-116">Specifies that the [ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) method will obtain the collection of range objects that cover the text changed during the edit session.</span></span><br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <span data-ttu-id="f85fd-117"><dt>**TF \_ \_Objeto HF**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-117"><dt>**TF\_HF\_OBJECT**</dt> <dt>( 1 )</dt></span></span> </dl>                                              | <span data-ttu-id="f85fd-118">O deslocamento de intervalo será interrompido se um objeto inserido for encontrado.</span><span class="sxs-lookup"><span data-stu-id="f85fd-118">The range shift stops if an embedded object is encountered.</span></span> <span data-ttu-id="f85fd-119">Usado no membro **dwFlags** da [estrutura \_ HALTCOND de TF](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .</span><span class="sxs-lookup"><span data-stu-id="f85fd-119">Used in **dwFlags** member of [TF\_HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) structure.</span></span><br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <span data-ttu-id="f85fd-120"><dt>**TF \_ \_Correção do IE**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-120"><dt>**TF\_IE\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="f85fd-121">O texto é uma transformação (correção) do conteúdo existente, para que outros serviços de texto possam preservar os dados associados ao texto original.</span><span class="sxs-lookup"><span data-stu-id="f85fd-121">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="f85fd-122">Usado no parâmetro *dwFlags* de [ITfRange:: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span><span class="sxs-lookup"><span data-stu-id="f85fd-122">Used in *dwFlags* parameter of [ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).</span></span><br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <span data-ttu-id="f85fd-123"><dt>**TF \_ \_Cookie inválido**</dt> <dt>(0xFFFFFFFF)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-123"><dt>**TF\_INVALID\_COOKIE**</dt> <dt>( 0xffffffff )</dt></span></span> </dl>                      | <span data-ttu-id="f85fd-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f85fd-124">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <span data-ttu-id="f85fd-125"><dt>**TF \_ \_ \_ Cookie de edição inválido**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-125"><dt>**TF\_INVALID\_EDIT\_COOKIE**</dt> <dt>( 0 )</dt></span></span> </dl>               | <span data-ttu-id="f85fd-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f85fd-126">Not used.</span></span><br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <span data-ttu-id="f85fd-127"><dt>**TF \_ POPF \_ todos**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-127"><dt>**TF\_POPF\_ALL**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                               | <span data-ttu-id="f85fd-128">Todos os contextos são removidos da pilha.</span><span class="sxs-lookup"><span data-stu-id="f85fd-128">All contexts are removed from the stack.</span></span> <span data-ttu-id="f85fd-129">Usado no parâmetro *dwFlags* de [ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span><span class="sxs-lookup"><span data-stu-id="f85fd-129">Used in *dwFlags* parameter of [ITfDocumentMgr::Pop](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).</span></span><br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <span data-ttu-id="f85fd-130"><dt>**TF \_ \_Correção de St**</dt> <dt>(1)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-130"><dt>**TF\_ST\_CORRECTION**</dt> <dt>( 1 )</dt></span></span> </dl>                                  | <span data-ttu-id="f85fd-131">O texto é uma transformação (correção) do conteúdo existente, para que outros serviços de texto possam preservar os dados associados ao texto original.</span><span class="sxs-lookup"><span data-stu-id="f85fd-131">The text is a transform (correction) of existing content, so that other text services can preserve data associated with the original text.</span></span> <span data-ttu-id="f85fd-132">Usado no parâmetro *dwFlags* de [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span><span class="sxs-lookup"><span data-stu-id="f85fd-132">Used in *dwFlags* parameter of [ITfRange::SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).</span></span><br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <span data-ttu-id="f85fd-133"><dt>**TF \_ \_Correção da tu**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-133"><dt>**TF\_TU\_CORRECTION**</dt> <dt>( 0x1 )</dt></span></span> </dl>                                | <span data-ttu-id="f85fd-134">A alteração de texto é o resultado de uma transformação (correção) do conteúdo existente.</span><span class="sxs-lookup"><span data-stu-id="f85fd-134">The text change is the result of a transform (correction) of existing content.</span></span> <span data-ttu-id="f85fd-135">Isso significa que a semântica do texto não foi alterada.</span><span class="sxs-lookup"><span data-stu-id="f85fd-135">This implies that the semantics of the text have not changed.</span></span> <span data-ttu-id="f85fd-136">Usado no parâmetro *dwFlags* de [ITfPropertyStore:: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span><span class="sxs-lookup"><span data-stu-id="f85fd-136">Used in *dwFlags* parameter of [ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).</span></span><br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <span data-ttu-id="f85fd-137"><dt>**TF \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-137"><dt>**TF\_US\_HIDETIPUI**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="f85fd-138">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f85fd-138">Not used.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="f85fd-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f85fd-139">Requirements</span></span>



| <span data-ttu-id="f85fd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="f85fd-140">Requirement</span></span> | <span data-ttu-id="f85fd-141">Valor</span><span class="sxs-lookup"><span data-stu-id="f85fd-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f85fd-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f85fd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="f85fd-143">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f85fd-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f85fd-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f85fd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="f85fd-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f85fd-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f85fd-146">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f85fd-146">Redistributable</span></span><br/>          | <span data-ttu-id="f85fd-147">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f85fd-147">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="f85fd-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f85fd-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f85fd-149"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-149"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="f85fd-150">INSERI</span><span class="sxs-lookup"><span data-stu-id="f85fd-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f85fd-151"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f85fd-151"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f85fd-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="f85fd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f85fd-153">ITextStoreACP:: getseleções</span><span class="sxs-lookup"><span data-stu-id="f85fd-153">ITextStoreACP::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[<span data-ttu-id="f85fd-154">ITextStoreAnchor:: getseleções</span><span class="sxs-lookup"><span data-stu-id="f85fd-154">ITextStoreAnchor::GetSelection</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[<span data-ttu-id="f85fd-155">ITfContext:: getseleções</span><span class="sxs-lookup"><span data-stu-id="f85fd-155">ITfContext::GetSelection</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[<span data-ttu-id="f85fd-156">ITfDocumentMgr::P op</span><span class="sxs-lookup"><span data-stu-id="f85fd-156">ITfDocumentMgr::Pop</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[<span data-ttu-id="f85fd-157">ITfEditRecord::GetTextAndPropertyUpdates</span><span class="sxs-lookup"><span data-stu-id="f85fd-157">ITfEditRecord::GetTextAndPropertyUpdates</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[<span data-ttu-id="f85fd-158">ITfPropertyStore::OnTextUpdated</span><span class="sxs-lookup"><span data-stu-id="f85fd-158">ITfPropertyStore::OnTextUpdated</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[<span data-ttu-id="f85fd-159">ITfRange::InsertEmbedded</span><span class="sxs-lookup"><span data-stu-id="f85fd-159">ITfRange::InsertEmbedded</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[<span data-ttu-id="f85fd-160">ITfRange:: SetText</span><span class="sxs-lookup"><span data-stu-id="f85fd-160">ITfRange::SetText</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[<span data-ttu-id="f85fd-161">TfClientId</span><span class="sxs-lookup"><span data-stu-id="f85fd-161">TfClientId</span></span>](tfclientid.md)
</dt> <dt>

[<span data-ttu-id="f85fd-162">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="f85fd-162">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="f85fd-163">TF \_ HALTCOND</span><span class="sxs-lookup"><span data-stu-id="f85fd-163">TF\_HALTCOND</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





