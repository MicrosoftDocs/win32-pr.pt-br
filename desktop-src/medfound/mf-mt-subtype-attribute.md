---
description: GUID de subtipo para um tipo de mídia.
ms.assetid: 8e600943-92f1-4936-8c00-842fc7f4cb57
title: Atributo MF_MT_SUBTYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f156e356a0e80d6b2c4bff1ae6f266e4d64b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011097"
---
# <a name="mf_mt_subtype-attribute"></a>\_Atributo de \_ subtipo MF MT

GUID de subtipo para um tipo de mídia.

## <a name="data-type"></a>Tipo de dados

**GUID**

## <a name="remarks"></a>Comentários

O GUID de subtipo define um tipo de formato de mídia específico dentro de um tipo principal. Por exemplo, no vídeo, os subtipos incluem RGB-24, RGB-32, UYVY, AYUV e assim por diante. No áudio, os subtipos incluem áudio PCM, áudio do Windows Media 9 e assim por diante.

Para obter os valores possíveis, consulte os seguintes tópicos:

-   [GUIDs de subtipo de áudio](audio-subtype-guids.md)
-   [GUIDs de subtipo de vídeo](video-subtype-guids.md)

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




