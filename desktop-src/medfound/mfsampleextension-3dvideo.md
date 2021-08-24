---
description: Especifica se um exemplo de mídia contém um quadro de vídeo 3D.
ms.assetid: 1B0B9DBD-80EB-4876-B2F2-BE419AC84265
title: Atributo MFSampleExtension_3DVideo (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb959accfb3326e90068a26247eeab25e9aeaddacb720a0dfd64aa6e5b237a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722796"
---
# <a name="mfsampleextension_3dvideo-attribute"></a>\_Atributo MFSampleExtension 3DVideo

Especifica se um exemplo de mídia contém um quadro de vídeo 3D.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Se esse atributo for **true**, o exemplo de mídia conterá um quadro de vídeo com duas ou mais exibições estereoscópico. O valor padrão é **FALSE**.

Um componente que gera quadros de vídeo 3D deve definir esse atributo como **true** em cada amostra de mídia que contenha um quadro 3D.

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

[MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)
</dt> </dl>

 

 




