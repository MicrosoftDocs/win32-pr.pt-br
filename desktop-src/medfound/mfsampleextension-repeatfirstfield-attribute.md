---
description: Especifica se o primeiro campo deve ser repetido em um quadro entrelaçado. Esse atributo se aplica a exemplos de mídia.
ms.assetid: c469f418-fa23-443f-8012-0d548ee98c17
title: Atributo MFSampleExtension_RepeatFirstField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0af10157c280a3e48ed8f415529534fc97fd5cc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091056"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



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

 

 




