---
description: Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado. Esse atributo se aplica a exemplos de mídia.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Atributo MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f0668e37e6a6958615c83f98c4b6b87eb170b115cf0549f3944a43b21c5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117872416"
---
# <a name="mfsampleextension_repeatfirstfield-attribute"></a>\_Atributo MFSampleExtension RepeatFirstField

Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado. Esse atributo se aplica a exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Se o valor for **false** ou o atributo não estiver definido, o primeiro campo não será repetido. Se o valor for **true**, o primeiro campo será repetido. O valor **true** é válido somente quando as seguintes condições são verdadeiras:

-   O tipo de mídia é entrelaçado misto e progressivo. (O atributo de atributo do [**\_ \_ \_ modo de entrelaçamento MF MT**](mf-mt-interlace-mode-attribute.md) no tipo de mídia é **MFVideoInterlace \_ MixedInterlaceOrProgressive**.)
-   O quadro é progressivo e o atributo [**\_ entrelaçado MFSampleExtension**](mfsampleextension-interlaced-attribute.md) no exemplo é **true**.
-   O atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) é definido no exemplo. O valor pode ser **true** ou **false**. A ordenação dos campos é determinada por esse atributo.

Esse atributo é usado para a busca de 3:2. A tabela a seguir mostra a ordem na qual os campos são exibidos.



| MFSampleExtension \_ RepeatFirstField | MFSampleExtension \_ BottomFieldFirst | Ordem dos campos         |
|-------------------------------------|-------------------------------------|---------------------|
| **TRUE**                            | **TRUE**                            | Inferior, superior, inferior |
| **TRUE**                            | **FALSE**                           | Superior, inferior, superior |
| **FALSE**                           | **TRUE**                            | Inferior, superior        |
| **FALSE**                           | **FALSE**                           | Superior, inferior        |



 

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

[Atributos de exemplo](sample-attributes.md)
</dt> <dt>

[Amostras de mídia](media-samples.md)
</dt> <dt>

[Entrelaçamento de vídeo](video-interlacing.md)
</dt> </dl>

 

 




