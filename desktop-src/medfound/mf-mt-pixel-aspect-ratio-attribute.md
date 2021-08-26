---
description: Taxa de proporção de pixel para um tipo de mídia de vídeo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Atributo MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e14e07a8011f89d16b095728bc80cbe19faa16ef9427156868f93c2ccb412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060486"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>\_Atributo de \_ \_ taxa de proporção MF MT pixel \_

Taxa de proporção de pixel para um tipo de mídia de vídeo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Os bits superiores de 32 contêm o numerador da taxa de proporção de pixel e os bits inferiores de 32 contêm o denominador. O numerador é o componente horizontal da taxa de proporção; o denominador é o componente vertical.

Para definir esse atributo, use a função [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Para obter esse atributo, use a função [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

A taxa de proporção de pixel descreve a forma dos pixels na imagem de vídeo exibida. Defina esse atributo se a imagem tiver pixels não quadrados. Para exibir corretamente em um dispositivo de vídeo com pixels quadrados, a imagem deve ser dimensionada pelo inverso da taxa de proporção de pixel da imagem.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Taxa de proporção da imagem](picture-aspect-ratio.md)
</dt> </dl>

 

 




