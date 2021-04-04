---
title: Constantes de TS_IE_ (Textstor. h)
description: As \_ constantes TS IE \_ \ descrevem como inserir texto que pode conter objetos inseridos usados pelos serviços de texto.
ms.assetid: a455d712-42d5-472e-862d-85ae3ba9149f
topic_type:
- apiref
api_name:
- TS_IE_CORRECTION
- TS_IE_COMPOSITION
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9abdb05ba065ed9bf41b5379060c0643053884e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085364"
---
# <a name="ts_ie_-constants"></a>Constantes de TS \_ IE \_ \*

As \_ constantes TS IE \_ \* descrevem como inserir texto que pode conter objetos incorporados usados pelos serviços de texto.



| Constante/valor                                                                                                                                                                                                                          | Descrição                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IE_CORRECTION"></span><span id="ts_ie_correction"></span><dl> <dt>**TS \_ \_Correção do IE**</dt> <dt>(0x1)</dt> </dl>    | O texto é uma transformação (correção) do conteúdo existente e qualquer informação especial de marcação de texto (metadados) é mantida, como dados de arquivo. wav ou um identificador de idioma.<br/> |
| <span id="TS_IE_COMPOSITION"></span><span id="ts_ie_composition"></span><dl> <dt>**TS \_ \_Composição do IE**</dt> <dt>(0x2)</dt> </dl> | Não usado.<br/>                                                                                                                                                                  |



## <a name="remarks"></a>Comentários

Essas constantes são usadas no parâmetro *dwFlags* de [ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded) e [ITextStoreAnchor:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded).

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

[ITextStoreACP:: InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembedded)
</dt> <dt>

[ITextStoreAnchor::InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded)
</dt> </dl>

 

 





