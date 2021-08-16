---
description: Especifica, em IMFTransform, a taxa máxima de processamento de macroblock, em macroblocks por segundo, que é suportada pelo codificador de hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c76e6a44a6e0993f9cf6410a0092708da767f92815fc98020dd2f4d88359370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739234"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>Atributo MF \_ VIDEO MAX MB PER \_ \_ \_ \_ SEC

Especifica, em [**IMFTransform,**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)a taxa máxima de processamento de macroblock, em macroblocks por segundo, que é suportada pelo codificador de hardware.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Este é um atributo somente leitura.

**Codificadores H.264/AVC:**

Esse atributo é afetado pelas seguintes propriedades:

-   [MF \_ MT \_ VIDEO \_ LEVEL](mf-mt-video-level.md) (que é um alias [de MF \_ MT \_ MPEG2 \_ LEVEL](mf-mt-mpeg2-level-attribute.md))
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Se o [atributo \_ MF MT \_ VIDEO \_ LEVEL](mf-mt-video-level.md) estiver presente, o codificador deverá retornar a taxa de processamento para a taxa de bits e resolução mais altas com suporte no nível especificado. Se o atributo \_ MF MT VIDEO LEVEL não estiver presente, ele \_ deverá usar um nível padrão de \_ 4.

Se a propriedade ICodecAPI [ \_ CODECAPI AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) tiver sido definida, o codificador deverá retornar a taxa de processamento correspondente ao valor definido para essa propriedade. Se o atributo CODECAPI AVEncCommonQualityVsSpeed não estiver presente, ele deverá usar um valor padrão de 0, que deve ser o modo de processamento mais \_ rápido.

Se a propriedade [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI tiver sido definida como um valor válido e com suporte, o codificador deverá retornar a taxa de processamento correspondente ao valor definido para essa propriedade. Se o atributo CODECAPI AVEncMPVDefaultBPictureCount não for presen, ele deverá usar um valor padrão de \_ 0 B quadros.

Somente os 28 bits inferiores devem ser usados por um aplicativo. Os 4bits superiores são reservados para uso futuro. Os aplicativos devem ignorar os 4 bits superiores e os MFTs devem definir os 4 bits superiores como 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
