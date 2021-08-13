---
description: Para um formato de vídeo 3D, especifica qual exibição é a exibição de base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Atributo MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb03bc12d32b96abc52999ef6a3b21580c4ac1c59125a076b9eb1d620e0bd362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741588"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




