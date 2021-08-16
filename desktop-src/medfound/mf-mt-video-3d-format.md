---
description: Para um tipo de mídia de vídeo, especifica como os quadros de vídeo 3D são armazenados na memória.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4100a605ecc7e8fe1c171b02341822972061363e7cd1b322162291dbd75b2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692065"
---
# <a name="mf_mt_video_3d_format-attribute"></a>Atributo \_ MF MT \_ VIDEO \_ 3D \_ FORMAT

Para um tipo de mídia de vídeo, especifica como os quadros de vídeo 3D são armazenados na memória.

## <a name="data-type"></a>Tipo de dados

**MFVideo3DFormat** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da [**enumeração MFVideo3DFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) O atributo se aplicará somente se o atributo [ \_ MF MT \_ VIDEO \_ 3D](mf-mt-video-3d.md) for **TRUE.**

Esse atributo é necessário para formatos de vídeo 3D descompactados. Ele é opcional para vídeo 3D compactado. Uma fonte de mídia que fornece quadros codificados pode ser capaz de definir o atributo, com base nas informações no contêiner de arquivos. Caso contrário, o atributo deve ser definido pelo decodificador no tipo de mídia de saída do decodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




