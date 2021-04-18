---
description: Contém o carimbo de data/hora de decodificação (DTS) para o exemplo.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: Atributo MFSampleExtension_DecodeTimestamp (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9676b295eb16e7cb2bb607ef4a5074d24b276d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781111"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>\_Atributo MFSampleExtension DecodeTimestamp

Contém o carimbo de data/hora de decodificação (DTS) para o exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

O valor do atributo é o DTS em unidades de 100 nanossegundos. O DTS é definido em alguns padrões de codificação, incluindo MPEG. O DTS especifica quando a imagem codificada deve ser decodificada. Se o vídeo codificado contiver quadros B, o DTS poderá ser diferente do horário da apresentação, porque as imagens B aparecem fora de ordem temporal no fragmentado.

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

[Atributos de exemplo](sample-attributes.md)
</dt> </dl>

 

 




