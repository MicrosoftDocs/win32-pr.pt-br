---
title: Constantes de TS_ATTR_ (Textstor. h)
description: As \_ constantes TS attr \_ \ são usadas para obter e alterar os valores dos atributos do documento. Essas constantes formam possíveis valores de sinalizadores de campo de bits nos métodos ITextStoreACP e ITextStoreAnchor.
ms.assetid: e99a44ba-c41a-4dd7-9475-dd37159081fd
topic_type:
- apiref
api_name:
- TS_ATTR_FIND_BACKWARDS
- TS_ATTR_FIND_WANT_OFFSET
- TS_ATTR_FIND_UPDATESTART
- TS_ATTR_FIND_WANT_VALUE
- TS_ATTR_FIND_WANT_END
- TS_ATTR_FIND_HIDDEN
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa26b8a725475a3d88b07cce1dccd0ac7fa1a98e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455573"
---
# <a name="ts_attr_-constants"></a>\_Constantes de atributo TS \_ \*

As \_ constantes de atributo TS \_ \* são usadas para obter e alterar os valores dos atributos do documento. Essas constantes formam possíveis valores de sinalizadores de campo de bits nos métodos [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) e [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .



| Constante/valor                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_ATTR_FIND_BACKWARDS"></span><span id="ts_attr_find_backwards"></span><dl> <dt>**TS \_ ATTR \_ localizar \_ versões anteriores**</dt> <dt>(0x1)</dt> </dl>        | Pesquisar retroativamente a partir do caractere inicial ou da posição da âncora para a posição em que ocorre uma transição em um valor de atributo de documento. O padrão é Pesquisar em frente.<br/>                                                                                                                                                                                    |
| <span id="TS_ATTR_FIND_WANT_OFFSET"></span><span id="ts_attr_find_want_offset"></span><dl> <dt>**TS \_ Atributo de \_ localização de local \_ \_ attr**</dt> <dt>(0x2)</dt> </dl> | Retorna o número de caracteres entre o caractere inicial ou a posição da âncora (**acpStart** em [ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition) ou **PaStart** em [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) ) e a posição na qual ocorre uma transição de atributo.<br/> |
| <span id="TS_ATTR_FIND_UPDATESTART"></span><span id="ts_attr_find_updatestart"></span><dl> <dt>**TS \_ ATTR \_ localizar \_ UPDATESTART**</dt> <dt>(0x4)</dt> </dl>  | Usado por [ITextStoreAnchor:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition) para posicionar a âncora de entrada na próxima transição de atributo, se uma for encontrada. Caso contrário, a âncora de entrada não será modificada.<br/>                                                                                                                             |
| <span id="TS_ATTR_FIND_WANT_VALUE"></span><span id="ts_attr_find_want_value"></span><dl> <dt>**TS \_ Atributo \_ de \_ localização \_ do attr**</dt> <dt>(0x8)</dt> </dl>    | Carregue os valores de atributo de documento com suporte na estrutura [TS \_ ATTRVAL](/windows/desktop/api/Textstor/ns-textstor-ts_attrval) .<br/>                                                                                                                                                                                                                                                              |
| <span id="TS_ATTR_FIND_WANT_END"></span><span id="ts_attr_find_want_end"></span><dl> <dt>**TS \_ \_ \_ \_ Término da localização**</dt> de ' attr ' <dt>(0x10)</dt> </dl>         | Usado por [ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition) e [ITextStoreAnchor:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition) para obter os valores de atributo de documento que terminam no caractere ou posição de âncora especificada.<br/>               |
| <span id="TS_ATTR_FIND_HIDDEN"></span><span id="ts_attr_find_hidden"></span><dl> <dt>**TS \_ ATTR \_ localizar \_ oculto**</dt> <dt>(0x20)</dt> </dl>                | Reservado.<br/>                                                                                                                                                                                                                                                                                                                                               |



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

[\_ATTRID TS](ts-attrid.md)
</dt> <dt>

[\_ATTRVAL TS](/windows/desktop/api/Textstor/ns-textstor-ts_attrval)
</dt> <dt>

[ITextStoreACP:: FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-findnextattrtransition)
</dt> <dt>

[ITextStoreACP:: RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition)
</dt> <dt>

[ITextStoreAnchor::FindNextAttrTransition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-findnextattrtransition)
</dt> <dt>

[ITextStoreAnchor::RequestAttrsTransitioningAtPosition](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition)
</dt> </dl>

 

 





