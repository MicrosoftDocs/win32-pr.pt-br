---
description: Relata os metadados e o buffer de máscara para uma máscara de segmentação em segundo plano que distingue entre o plano de fundo e o primeiro plano de um quadro de vídeo.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK atributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691835"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a>Atributo MF \_ CAPTURE \_ METADATA \_ FRAME BACKGROUND \_ \_ MASK

Relata os metadados e o buffer de máscara para uma máscara de segmentação em segundo plano que distingue entre o plano de fundo e o primeiro plano de um quadro de vídeo.

## <a name="data-type"></a>Tipo de dados

**Blob**

## <a name="remarks"></a>Comentários

Os dados carregados por esse atributo são uma estrutura KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK que contém informações sobre as dimensões da máscara em segundo plano, bem como sua cobertura do quadro do qual ele é inferido, que é [o](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) quadro que é produzido pelo fluxo. Ele também carrega um buffer contíguo que representa a máscara a ser aproveitada pelo aplicativo consumidor para definir quais pixels são considerados parte do primeiro plano ou da tela de fundo. O dimensionamento e a correlação de coordenadas de imagem da máscara em relação ao quadro são tratados pelo aplicativo consumidor. 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Build 22000t<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Build 22000<br/>                      |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 




