---
description: Contém um GUID de formato do DirectShow para um tipo de mídia.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: Atributo MF_MT_AM_FORMAT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18a8faf88128075e5c5b51c1b5ace39329d4e1fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296563"
---
# <a name="mf_mt_am_format_type-attribute"></a>\_Atributo de \_ \_ tipo de formato MF MT am \_

Contém um GUID de formato do DirectShow para um tipo de mídia.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido quando um tipo de mídia do DirectShow é convertido em um tipo de mídia Media Foundation. O atributo indica o tipo de formato do DirectShow original. O valor corresponde ao membro formatType da estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

Para um formato de áudio, o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) pode conter o bloco de formato original, se o tipo de formato do DirectShow não foi reconhecido.

Não defina esse atributo em um tipo de mídia, a menos que você esteja convertendo uma estrutura de formato do DirectShow.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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

 

 
