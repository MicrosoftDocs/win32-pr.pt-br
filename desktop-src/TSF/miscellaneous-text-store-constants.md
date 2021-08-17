---
title: Constantes de armazenamento de texto diversos (Textstor.h)
description: As constantes de armazenamento de texto diversos configuram determinadas propriedades para armazenamentos de texto.
ms.assetid: 6e05ed74-fff3-4bc4-a21e-9af9492af23b
topic_type:
- apiref
api_name:
- TS_DEFAULT_SELECTION
- TS_GEA_HIDDEN
- TS_GTA_HIDDEN
- TS_ST_CORRECTION
- TS_TC_CORRECTION
- TS_VCOOKIE_NUL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55bfa06f7f0ebda1d572a4e637076de25c7a21ef4d273cdc2527ab6481393404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952094"
---
# <a name="miscellaneous-text-store-constants"></a>Constantes de armazenamento de texto diversos

As constantes de armazenamento de texto diversos configuram determinadas propriedades para armazenamentos de texto.



| Constante/valor                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ SELEÇÃO \_ PADRÃO**</dt> <dt>( ( ULONG )-1 )</dt> </dl> | Se o *parâmetro ulIndex* [de ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) for definido com esse valor, a seleção padrão será obtida.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ GEA \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | Se *o parâmetro dwFlags* [de ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) for definido com esse valor, um objeto inserido poderá ser localizado em texto oculto.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ "? \_ HIDDEN**</dt> <dt>( 0x1 )</dt> </dl>                              | Não usado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ ST \_ CORRECTION**</dt> <dt>( 0x1 )</dt> </dl>                     | Se o parâmetro *dwFlags* [de ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)ou [ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) for definido como esse valor, o texto será uma transformação (correção) do conteúdo existente e quaisquer informações especiais de marcação de texto (metadados) serão mantidas, como dados de arquivo .wav ou um identificador de idioma.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ CORREÇÃO \_ de TC**</dt> <dt>( 0x1 )</dt> </dl>                     | Se o parâmetro *dwFlags* [de ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) for definido com esse valor, o texto será uma transformação (correção) do conteúdo existente e quaisquer informações especiais de marcação de texto (metadados) serão mantidas, como dados de arquivo .wav ou um identificador de idioma.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCOOKIE \_ NUL**</dt> <dt>( 0xffffffff )</dt> </dl>                    | Usado internamente pelo TSF.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Textstor.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Textstor.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfContext::GetSelection](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor::SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor::GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Constantes de estrutura diversas](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





