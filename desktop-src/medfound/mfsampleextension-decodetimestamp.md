---
description: Contém o carimbo de data/hora de decodificar (DTS) para o exemplo.
ms.assetid: 4E0B8266-FF48-49A1-AB7B-A47C4F96AECD
title: MFSampleExtension_DecodeTimestamp atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e0d72ea69f487efe24148fa8ce60ad05eb7a124673f02a78e70c67f604a51bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241477"
---
# <a name="mfsampleextension_decodetimestamp-attribute"></a>Atributo MFSampleExtension \_ DecodeTimestamp

Contém o carimbo de data/hora de decodificar (DTS) para o exemplo.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

O valor do atributo é o DTS em unidades de 100 nanossegundos. O DTS é definido em alguns padrões de codificação, incluindo MPEG. O DTS especifica quando a imagem codificada deve ser decodificada. Se o vídeo codificado contiver quadros B, o DTS poderá ser diferente do tempo de apresentação, pois as imagens B aparecem fora da ordem temporal no bitstream.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de exemplo](sample-attributes.md)
</dt> </dl>

 

 




