---
description: Define a abertura de exibição, que é a região de um quadro de vídeo que contém dados de imagem válidos.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Atributo MF_MT_MINIMUM_DISPLAY_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768357"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>\_Atributo de \_ \_ abertura de exibição mínima \_ de MF MT

Define a abertura de exibição, que é a região de um quadro de vídeo que contém dados de imagem válidos.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor do atributo é uma estrutura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

A abertura de exibição mínima é a região que contém a parte válida do sinal. Os pixels fora da abertura contêm dados inválidos e não devem ser exibidos.

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

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Taxa de proporção da imagem](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ abertura geométrica do MF MT \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**\_abertura de \_ digitalização de Pan MT \_ MF \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




