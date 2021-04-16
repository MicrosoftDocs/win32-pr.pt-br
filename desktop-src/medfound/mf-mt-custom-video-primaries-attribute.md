---
description: Especifica primárias de cores personalizadas para um tipo de mídia de vídeo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Atributo MF_MT_CUSTOM_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782379"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a>\_Atributo de \_ \_ \_ primários de vídeo de MF MT

Especifica primárias de cores personalizadas para um tipo de mídia de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Matriz de bytes

## <a name="remarks"></a>Comentários

Os dados de atributo são uma estrutura [**\_ primária de \_ vídeo \_ de MT personalizado**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .

Esse atributo especifica o volume de cor real de conteúdo ou uma exibição. As informações de Master volume de cores CEA-861,3/SMPTE ST. 2086 são armazenadas nesse atributo por decodificadores. Observe que esse atributo não substitui o atributo [**de \_ \_ \_ primárias de vídeo MF MT**](mf-mt-video-primaries-attribute.md). Esse atributo descreve uma dica sobre o volume de cores do conteúdo, enquanto **os \_ \_ \_ primários de vídeo MF MT** descrevem os primários de cor nos quais o conteúdo é realmente codificado (por exemplo: o significado de 1,0 nos canais R/g/B de uma representação de ponto flutuante).

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

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




