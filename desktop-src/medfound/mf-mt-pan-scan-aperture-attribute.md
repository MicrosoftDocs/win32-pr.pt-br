---
description: Define a abertura de panorâmica/digitalização, que é a 4&\# 215; 3 região de vídeo que deve ser exibida no modo de panorâmica/digitalização.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Atributo MF_MT_PAN_SCAN_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781345"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>\_Atributo de \_ \_ abertura de digitalização de Pan MT MF \_

Define a abertura de panorâmica/digitalização, que é a área de vídeo de 4 × 3 que deve ser exibida no modo de panorâmica/digitalização.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor do atributo é uma estrutura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Esse atributo é usado para cortar o vídeo widescreen em uma taxa de proporção de 4:3. A abertura de panorâmica/verificação é usada somente no modo de panorâmica/digitalização, que é habilitado definindo o atributo [**MF de \_ \_ Pan \_ \_ MT**](mf-mt-pan-scan-enabled-attribute.md) para **true**.

Se o modo de panorâmica/verificação não estiver habilitado, use a abertura de exibição, especificada pelo atributo de [**\_ \_ \_ \_ abertura de exibição mínima de MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Se esse atributo não for definido, a abertura de panorâmica/verificação será considerada como o quadro de vídeo inteiro.

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

[**\_abertura de \_ \_ exibição mínima \_ de MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_exame de Pan MT do MF \_ \_ \_ habilitado**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




