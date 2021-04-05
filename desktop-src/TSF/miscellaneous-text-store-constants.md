---
title: Constantes de armazenamento de texto diversos (Textstor. h)
description: As constantes de armazenamento de texto diversos definem determinadas propriedades para armazenamentos de texto.
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
ms.openlocfilehash: ead33c21bb78035dd9fda443a53de575ffa64d9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086129"
---
# <a name="miscellaneous-text-store-constants"></a>Constantes de armazenamento de texto diversos

As constantes de armazenamento de texto diversos definem determinadas propriedades para armazenamentos de texto.



| Constante/valor                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_DEFAULT_SELECTION"></span><span id="ts_default_selection"></span><dl> <dt>**TS \_ \_Seleção padrão**</dt> <dt>((ULong)-1)</dt> </dl> | Se o parâmetro *ulIndex* de [ITfContext::](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection) GetQuery for definido como esse valor, a seleção padrão será obtida.<br/>                                                                                                                                                                                                                                                                      |
| <span id="TS_GEA_HIDDEN"></span><span id="ts_gea_hidden"></span><dl> <dt>**TS \_ GEA \_ Hidden**</dt> <dt>(0x1)</dt> </dl>                              | Se o parâmetro *dwFlags* de [ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) for definido como esse valor, um objeto inserido poderá ser localizado dentro do texto oculto.<br/>                                                                                                                                                                                                                                             |
| <span id="TS_GTA_HIDDEN"></span><span id="ts_gta_hidden"></span><dl> <dt>**TS \_ GTA \_ oculto**</dt> <dt>(0x1)</dt> </dl>                              | Não usado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TS_ST_CORRECTION"></span><span id="ts_st_correction"></span><dl> <dt>**TS \_ \_**</dt> <dt>(0x1)</dt> </dl>                     | Se o parâmetro *dwFlags* de [ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext), [ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)ou [ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange) for definido como esse valor, o texto será uma transformação (correção) do conteúdo existente e quaisquer informações especiais de marcação de texto (metadados) serão mantidas, como dados de arquivo. wav ou um identificador de idioma.<br/> |
| <span id="TS_TC_CORRECTION"></span><span id="ts_tc_correction"></span><dl> <dt>**TS \_ \_Correção de TC**</dt> <dt>(0x1)</dt> </dl>                     | Se o parâmetro *dwFlags* de [ITextStoreAnchorSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange) for definido com esse valor, o texto será uma transformação (correção) do conteúdo existente e quaisquer informações especiais de marcação de texto (metadados) serão mantidas, como dados de arquivo. wav ou um identificador de idioma.<br/>                                                                                                              |
| <span id="TS_VCOOKIE_NUL"></span><span id="ts_vcookie_nul"></span><dl> <dt>**TS \_ VCOOKIE \_ nul**</dt> <dt>(0xFFFFFFFF)</dt> </dl>                    | Usado internamente pelo TSF.<br/>                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITfContext:: getseleções](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getselection)
</dt> <dt>

[ITextStoreACP:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-settext)
</dt> <dt>

[ITextStoreAnchor:: SetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-settext)
</dt> <dt>

[ITextStoreAnchor:: getembedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded)
</dt> <dt>

[ITextStoreACPSink:: OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-ontextchange)
</dt> <dt>

[ITextStoreAnchorSink::OnTextChange](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-ontextchange)
</dt> <dt>

[Constantes de estrutura diversas](miscellaneous-framework-constants.md)
</dt> </dl>

 

 





