---
description: Para um formato de vídeo 3D, especifica qual exibição é a exibição à esquerda.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Atributo MF_MT_VIDEO_3D_FIRST_IS_LEFT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b7deed122f3de419455abf54bfcc18ad50ef199d87afa8bcaad8d34000a011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876797"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>O \_ \_ atributo 3D de vídeo MF MT \_ \_ First \_ é \_ Left

Para um formato de vídeo 3D, especifica qual exibição é a exibição à esquerda.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Para vídeo 3D, cada amostra de vídeo contém duas exibições, que são designadas *primeira exibição* e *segunda exibição*. O layout exato das exibições na memória é indicado pelo atributo [de \_ \_ \_ \_ formato 3D de vídeo MF MT](mf-mt-video-3d-format.md) .



| Formatar               | Primeira exibição              | Segunda exibição               |
|----------------------|-------------------------|---------------------------|
| Empacotado lado a lado  | Metade esquerda do buffer | Metade direita do buffer  |
| De cima para baixo embalado | Metade superior do buffer  | Metade inferior do buffer |
| Visões            | Índice de buffer 0          | Índice de buffer 1            |
| Exibição de base            | Quadro inteiro            | Não está presente               |



 

Por padrão, a primeira exibição é a exibição à esquerda e a segunda exibição é a exibição correta. Se os modos de exibição esquerdo e direito forem trocados, defina \_ o \_ atributo MF MT Video \_ 3D \_ primeiro \_ is \_ Left como **false** no tipo de mídia.

> [!Note]  
> No formato de *exibição de base* (**MFVideo3DSampleFormat \_ BaseView**), somente a exibição de base é mantida, portanto, esse atributo não se aplica.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




