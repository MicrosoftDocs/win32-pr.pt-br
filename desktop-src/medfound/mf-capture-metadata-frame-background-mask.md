---
description: Relata os metadados e o buffer de máscara para uma máscara de segmentação de segundo plano que distingue entre o plano de fundo e o primeiro plano de um quadro de vídeo.
title: Atributo MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK (Mfapi. h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 1c9cf48235483f13cfa6f9fc04aace5baaf030cf1eb2597b86e9361176a0b9b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973975"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>Atributo de máscara de tela de fundo do MF \_ Capture \_ Metadata \_ frame \_ \_

Relata os metadados e o buffer de máscara para uma máscara de segmentação de segundo plano que distingue entre o plano de fundo e o primeiro plano de um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**BLOB**

## <a name="remarks"></a>Comentários

Os dados transmitidos por esse atributo são uma estrutura [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) que contém informações sobre as dimensões da máscara de plano de fundo, bem como sua cobertura do quadro do qual ela é inferida, que é o quadro que é disparado pelo fluxo. Ele também carrega um buffer contíguo que representa a máscara a ser utilizada pelo aplicativo de consumo para definir quais pixels são considerados parte do primeiro plano ou segundo plano. A correlação de escala e imagem coordenada da máscara em relação ao quadro é manipulada pelo aplicativo de consumo. 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Criar 22000t<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Build 22000<br/>                      |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 




