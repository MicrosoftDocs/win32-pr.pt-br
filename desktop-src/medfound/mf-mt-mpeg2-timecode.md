---
description: Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica que os pacotes de transporte contêm um código de tempo de 4 bytes.
ms.assetid: B172E7A8-5757-49B7-A784-FAFC7E904A4C
title: Atributo MF_MT_MPEG2_TIMECODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc9db5d7b3c6e94f7845bec2bd98c569d1b1f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170371"
---
# <a name="mf_mt_mpeg2_timecode-attribute"></a>Atributo de código de intróia MF \_ MT \_ \_

Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica que os pacotes de transporte contêm um código de tempo de 4 bytes.

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                                                | Significado                                                                                                                                        |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhum código de tempo é adicionado.<br/>                                                                                                              |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Um código de tempo de 4 bytes é adicionado no início de cada pacote de transporte. Esse código de tempo é exigido por alguns padrões de televisão digital.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




