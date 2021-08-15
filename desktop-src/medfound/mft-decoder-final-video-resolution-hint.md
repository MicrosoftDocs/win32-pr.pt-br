---
description: Especifica a resolução final de saída da imagem decodificada, após o processamento do vídeo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Atributo MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847a2925f2249c741e9a45a1dcc4826a1cbe3d6bb12cda4d8017ee0fb5de0069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973135"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a>\_Atributo de \_ \_ dica de resolução de vídeo final \_ do DEcodificador de MFT \_

Especifica a resolução final de saída da imagem decodificada, após o processamento do vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Há suporte para esse atributo em alguns decodificadores de vídeo. Um aplicativo pode definir esse atributo para indicar a largura e a altura da imagem após o processamento do vídeo. O decodificador pode usar essas informações para otimizar o processo de decodificação, especialmente se o tamanho final da imagem for muito menor do que o tamanho da imagem nativa. Por exemplo, o decodificador pode ignorar um filtro fora de loop.

Os bits superiores de 32 contêm a largura e os bits de 32 inferiores contêm a altura.

Para definir este atributo:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chame [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) para adicionar o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




