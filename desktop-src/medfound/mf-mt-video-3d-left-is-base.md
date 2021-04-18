---
description: Para um formato de vídeo 3D, especifica qual exibição é a exibição de base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Atributo MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785323"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>A \_ esquerda do vídeo MF MT \_ \_ 3D \_ é o \_ \_ atributo base

Para um formato de vídeo 3D, especifica qual exibição é a exibição de base.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Por padrão, a exibição à esquerda em uma sequência de vídeo 3D é a exibição de base. Se o modo de exibição à direita for o modo de exibição de base, defina esse atributo como **false**.

Para converter o vídeo estereoscópico em 2D, mantenha o modo de exibição de base e descarte o outro modo de exibição.

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

 

 




