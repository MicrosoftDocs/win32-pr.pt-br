---
description: Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.
ms.assetid: 1B996B22-C76B-47E5-8937-1E5E672E32EC
title: Atributo MFSampleExtension_3DVideo_SampleFormat (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14829c879c151149edc48bf1635b3a5591ddeac5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091360"
---
# <a name="mfsampleextension_3dvideo_sampleformat-attribute"></a>\_Atributo MFSampleExtension 3DVideo \_ SampleFormat

Especifica como um quadro de vídeo 3D é armazenado em um exemplo de mídia.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

O valor desse atributo é um membro da enumeração [**MFVideo3DSampleFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dsampleformat) .

Um componente que gera quadros de vídeo 3D deve definir esse atributo como **true** em cada amostra de mídia que contenha um quadro 3D. O atributo será ignorado se o atributo [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md) for **false** ou não estiver definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)
</dt> </dl>

 

 




