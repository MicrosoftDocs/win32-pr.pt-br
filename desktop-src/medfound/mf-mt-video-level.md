---
description: Especifica o nível MPEG-2 ou H. 264 em um tipo de mídia de vídeo. Este é um alias do \_ nível MF MT do \_ MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Atributo MF_MT_VIDEO_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785252"
---
# <a name="mf_mt_video_level-attribute"></a>\_Atributo de \_ nível de vídeo MF MT \_

Especifica o nível MPEG-2 ou H. 264 em um tipo de mídia de vídeo. Este é um alias do [ \_ \_ \_ nível MF MT do MPEG2](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

**Codificadores H. 264:**

Os níveis com suporte são estendidos para incluir o [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

Padrão: o padrão recomendado é selecionar o nível mínimo para corresponder à configuração de codificação de vídeo, incluindo a resolução, a taxa de quadros etc.

Padrão recomendado: selecione o nível mínimo para corresponder à configuração de codificação de vídeo, incluindo a resolução, a taxa de quadros, etc.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




