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
# <a name="miscellaneous-framework-constants"></a>Constantes de estrutura diversas

As constantes de estrutura diversas indicam configurações para clientes, processos ou texto.



| Constante/valor                                                                                                                                                                                                                                                      | Descrição                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_CLIENTID_NULL"></span><span id="tf_clientid_null"></span><dl> <dt>**TF \_ CLIENTID \_ nulo**</dt> <dt>((TfClientId) 0)</dt> </dl>                        | Indica para um serviço de texto que o cliente é desativado. Consulte [TfClientId](tfclientid.md).<br/>                                                                                                                                                      |
| <span id="TF_INVALID_GUIDATOM"></span><span id="tf_invalid_guidatom"></span><dl> <dt>**TF \_ \_GUIDATOM inválido**</dt> <dt>((TfGuidAtom) 0)</dt> </dl>               | O valor de [TfGuidAtom](tfguidatom.md) para o processo atual é inválido.<br/>                                                                                                                                                                         |
| <span id="TF_DEFAULT_SELECTION"></span><span id="tf_default_selection"></span><dl> <dt>**TF \_ \_seleção padrão**</dt> <dt>( \_ seleção padrão de TS \_ )</dt> </dl> | Use a seleção padrão. Usado por [ITfContext:: getseleções](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection), [ITextStoreACP:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)e [ITextStoreAnchor:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection).<br/>                |
| <span id="TF_GTP_INCL_TEXT"></span><span id="tf_gtp_incl_text"></span><dl> <dt>**TF \_ GTP \_ incl \_ Text**</dt> <dt>(0x1)</dt> </dl>                               | Especifica que o método [ITfEditRecord:: GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates) obterá a coleção de objetos Range que abrangem o texto alterado durante a sessão de edição.<br/>                                 |
| <span id="TF_HF_OBJECT"></span><span id="tf_hf_object"></span><dl> <dt>**TF \_ \_Objeto HF**</dt> <dt>(1)</dt> </dl>                                              | O deslocamento de intervalo será interrompido se um objeto inserido for encontrado. Usado no membro **dwFlags** da [estrutura \_ HALTCOND de TF](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond) .<br/>                                                                                                               |
| <span id="TF_IE_CORRECTION"></span><span id="tf_ie_correction"></span><dl> <dt>**TF \_ \_Correção do IE**</dt> <dt>(1)</dt> </dl>                                  | O texto é uma transformação (correção) do conteúdo existente, para que outros serviços de texto possam preservar os dados associados ao texto original. Usado no parâmetro *dwFlags* de [ITfRange:: InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded).<br/>                 |
| <span id="TF_INVALID_COOKIE"></span><span id="tf_invalid_cookie"></span><dl> <dt>**TF \_ \_Cookie inválido**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                      | Não usado.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_INVALID_EDIT_COOKIE"></span><span id="tf_invalid_edit_cookie"></span><dl> <dt>**TF \_ \_ \_ Cookie de edição inválido**</dt> <dt>(0)</dt> </dl>               | Não usado.<br/>                                                                                                                                                                                                                                          |
| <span id="TF_POPF_ALL"></span><span id="tf_popf_all"></span><dl> <dt>**TF \_ POPF \_ todos**</dt> <dt>(0x1)</dt> </dl>                                               | Todos os contextos são removidos da pilha. Usado no parâmetro *dwFlags* de [ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop).<br/>                                                                                                                             |
| <span id="TF_ST_CORRECTION"></span><span id="tf_st_correction"></span><dl> <dt>**TF \_ \_Correção de St**</dt> <dt>(1)</dt> </dl>                                  | O texto é uma transformação (correção) do conteúdo existente, para que outros serviços de texto possam preservar os dados associados ao texto original. Usado no parâmetro *dwFlags* de [ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext).<br/>                               |
| <span id="TF_TU_CORRECTION"></span><span id="tf_tu_correction"></span><dl> <dt>**TF \_ \_Correção da tu**</dt> <dt>(0x1)</dt> </dl>                                | A alteração de texto é o resultado de uma transformação (correção) do conteúdo existente. Isso significa que a semântica do texto não foi alterada. Usado no parâmetro *dwFlags* de [ITfPropertyStore:: OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated).<br/> |
| <span id="TF_US_HIDETIPUI"></span><span id="tf_us_hidetipui"></span><dl> <dt>**TF \_ US \_ HIDETIPUI**</dt> <dt>0x00000001</dt> </dl>                                | Não usado.<br/>                                                                                                                                                                                                                                          |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITextStoreACP:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getselection)
</dt> <dt>

[ITextStoreAnchor:: getseleções](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getselection)
</dt> <dt>

[ITfContext:: getseleções](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITfDocumentMgr::P op](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-pop)
</dt> <dt>

[ITfEditRecord::GetTextAndPropertyUpdates](/windows/desktop/api/Msctf/nf-msctf-itfeditrecord-gettextandpropertyupdates)
</dt> <dt>

[ITfPropertyStore::OnTextUpdated](/windows/desktop/api/Msctf/nf-msctf-itfpropertystore-ontextupdated)
</dt> <dt>

[ITfRange::InsertEmbedded](/windows/desktop/api/Msctf/nf-msctf-itfrange-insertembedded)
</dt> <dt>

[ITfRange:: SetText](/windows/desktop/api/Msctf/nf-msctf-itfrange-settext)
</dt> <dt>

[TfClientId](tfclientid.md)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[TF \_ HALTCOND](/windows/desktop/api/Msctf/ns-msctf-tf_haltcond)
</dt> </dl>

 

 





