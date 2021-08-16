---
description: Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: MFSampleExtension_3DVideo_SampleFormat atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6529a08c14846fb1d06cd9b3ed0827a43d1b1ba75310c0379efddadebecdaeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722866"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>Atributo MFSampleExtension \_ 3DVideo \_ SampleFormat

Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da [**enumeração MFVideo3DSampleFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat)

Um componente que gera quadros de vídeo 3D deve definir esse atributo como **TRUE** em cada amostra de mídia que contém um quadro 3D. O atributo será ignorado se o atributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) for **FALSE** ou não for definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




