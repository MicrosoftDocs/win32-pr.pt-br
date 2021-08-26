---
description: Especifica o nível MPEG-2 ou H.264 em um tipo de mídia de vídeo. Este é um alias de \_ MF MT \_ MPEG2 \_ LEVEL.
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: MF_MT_VIDEO_LEVEL atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b40f1ebc6834373e00253f494e3fc76c20c343af17d754c7c4fe642b802d16ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012766"
---
# <a name="mf_mt_video_level-attribute"></a>Atributo \_ MF MT \_ VIDEO \_ LEVEL

Especifica o nível MPEG-2 ou H.264 em um tipo de mídia de vídeo. Este é um alias do [ \_ MF MT \_ MPEG2 \_ LEVEL.](mf-mt-mpeg2-level-attribute.md)

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

**Codificadores H.264:**

Os níveis com suporte são estendidos para incluir [**o eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

Padrão: o padrão recomendado é selecionar o nível mínimo para corresponder à configuração de codificação de vídeo, incluindo resolução, taxa de quadros etc.

Padrão recomendado: selecione o nível mínimo para corresponder à configuração de codificação de vídeo, incluindo resolução, taxa de quadros etc.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




