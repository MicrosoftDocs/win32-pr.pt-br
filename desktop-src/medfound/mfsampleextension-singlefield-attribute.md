---
description: Especifica se um exemplo de vídeo contém um único campo ou dois campos intercalados. Esse atributo se aplica a exemplos de mídia.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Atributo MFSampleExtension_SingleField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502280"
---
# <a name="mfsampleextension_singlefield-attribute"></a>Atributo de MFSampleExtension \_ únicofield

Especifica se um exemplo de vídeo contém um único campo ou dois campos intercalados. Esse atributo se aplica a exemplos de mídia.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Aplica-se a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Comentários

Se o valor for **true**, o exemplo conterá um campo. Se o valor for **false** ou o atributo não estiver definido, o exemplo conterá um quadro completo. (Dois campos se entrelaçados ou um quadro progressivo).

Se o tipo de mídia for de quadros progressivos ou de campos intercalados, esse atributo deverá ser definido como **falso** ou esquerdo.

Se o tipo de mídia for um único campo, esse atributo deverá ser **true**. Defina o atributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) no exemplo para indicar se ele é o campo superior ou o campo inferior.

Atualmente, o processador de vídeo avançado (EVR) não oferece suporte a conteúdo que alterna entre quadros entrelaçados e campos únicos.

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

 

 




