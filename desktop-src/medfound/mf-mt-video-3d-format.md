---
description: Para um tipo de mídia de vídeo, especifica como os quadros de vídeo 3D são armazenados na memória.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Atributo MF_MT_VIDEO_3D_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757268"
---
# <a name="mf_mt_video_3d_format-attribute"></a>\_Atributo de \_ \_ formato 3D de vídeo MF MT \_

Para um tipo de mídia de vídeo, especifica como os quadros de vídeo 3D são armazenados na memória.

## <a name="data-type"></a>Tipo de dados

**MFVideo3DFormat** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da enumeração [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) . O atributo se aplicará somente se o atributo [ \_ \_ \_ 3D de vídeo MF MT](mf-mt-video-3d.md) for **true**.

Esse atributo é necessário para formatos de vídeo 3D não compactados. É opcional para vídeo 3D compactado. Uma fonte de mídia que fornece quadros codificados pode ser capaz de definir o atributo, com base nas informações no contêiner de arquivo. Caso contrário, o atributo deve ser definido pelo decodificador no tipo de mídia de saída do decodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




