---
description: Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica que os pacotes de transporte contêm um código de tempo de 4 byte.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: MF_MT_MPEG2_TIMECODE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7a4ce6868f783ed33c50acd5a8648297648481a58c74198b0dcadd1bd237bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741745"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>Atributo \_ MT \_ MPEG2 \_ TIMECODE

Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica que os pacotes de transporte contêm um código de tempo de 4 byte.

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhum código de hora é adicionado.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Um código de tempo de 4 byte é adicionado no início de cada pacote de transporte. Esse código de hora é exigido por alguns padrões de tv digital.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




