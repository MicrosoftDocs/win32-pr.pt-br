---
description: contém um GUID de formato DirectShow para um tipo de mídia.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Atributo MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff59e148f7532cc07e47acf033de91b5eaeb8969f0c39376850738fd54e758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973625"
---
# <a name="mf_mt_am_format_type-attribute"></a>\_Atributo de \_ \_ tipo de formato MF MT am \_

contém um GUID de formato DirectShow para um tipo de mídia.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

esse atributo pode ser definido quando um tipo de mídia DirectShow é convertido em um tipo de mídia Media Foundation. o atributo indica o tipo de formato de DirectShow original. O valor corresponde ao membro formatType da estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

para um formato de áudio, o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) pode conter o bloco de formato original, se o tipo de formato DirectShow não foi reconhecido.

não defina esse atributo em um tipo de mídia, a menos que você esteja convertendo uma estrutura de formato de DirectShow.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Conversões de tipo de mídia](media-type-conversions.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> <dt>

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
