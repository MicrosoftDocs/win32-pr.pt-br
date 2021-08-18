---
description: Especifica a rotação de um quadro de vídeo na direção do sentido anti-horário.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Atributo MF_MT_VIDEO_ROTATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf3d909b29757a02d46cc842b30f04bfb0463d6f734eecb74bfb957fa206fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876696"
---
# <a name="mf_mt_video_rotation-attribute"></a>\_Atributo de \_ rotação de vídeo MF MT \_

Especifica a rotação de um quadro de vídeo na direção do sentido anti-horário.

## <a name="data-type"></a>Tipo de dados

**MFVideoRotationFormat** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

O vídeo de um dispositivo portátil, como um telefone celular, geralmente é girado por 90, 180 ou 270 graus. Se a câmera armazenar a orientação como metadados no arquivo de vídeo, a imagem poderá ser ajustada no momento da reprodução.

Se esse atributo estiver definido como **MFVideoRotationFormat \_ 90**, isso significa que o conteúdo foi girado 90 graus na direção do sentido anti-horário. Se o conteúdo foi girado 90 graus na direção do sentido horário, o valor do atributo seria **MFVideoRotationFormat \_ 270**.

Os valores com suporte para esse atributo são enumerados em [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 




