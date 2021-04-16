---
description: Especifica, em IMFTransform, a taxa máxima de processamento de macrobloco, em macroblocos por segundo, que é suportada pelo codificador de hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Atributo MF_VIDEO_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768400"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>\_Atributo MF máximo de MB de vídeo \_ \_ \_ por \_ segundo

Especifica, em [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), a taxa máxima de processamento de macrobloco, em macroblocos por segundo, que é suportada pelo codificador de hardware.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Este é um atributo somente leitura.

**Codificadores H. 264/AVC:**

Esse atributo é afetado pelas seguintes propriedades:

-   [MF \_ \_ \_ Nível de vídeo MT](mf-mt-video-level.md) (que é um alias [do \_ \_ \_ nível de MPEG2 MF MT](mf-mt-mpeg2-level-attribute.md))
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Se o atributo de [ \_ nível de \_ vídeo \_ MF MT](mf-mt-video-level.md) estiver presente, o codificador deverá retornar a taxa de processamento para a taxa de bits e resolução mais altas com suporte no nível especificado. Se o \_ atributo de nível de vídeo MF MT \_ \_ não estiver presente, ele deverá usar um nível padrão de 4.

Se a propriedade [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI tiver sido definida, o codificador deverá retornar a taxa de processamento correspondente ao valor definido para essa propriedade. Se o \_ atributo CODECAPI AVEncCommonQualityVsSpeed não estiver presente, ele deverá usar um valor padrão de 0 que deve ser o modo de processamento mais rápido.

Se a propriedade [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI tiver sido definida como um valor válido e com suporte, o codificador deverá retornar a taxa de processamento correspondente ao valor definido para essa propriedade. Se o \_ atributo CODECAPI AVEncMPVDefaultBPictureCount não for, ele deverá usar um valor padrão de 0 B quadros.

Somente os 28 bits inferiores devem ser usados por um aplicativo. Os 4bits superiores são reservados para uso futuro. Os aplicativos devem ignorar os 4 bits superiores e MFTs deve definir os 4 bits superiores como 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
