---
description: Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica se os pacotes de transporte contêm cabeçalhos de pacote de conteúdo.
ms.assetid: 527B965D-4330-4DCB-B6DA-32D6BCDF5515
title: Atributo MF_MT_MPEG2_CONTENT_PACKET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acb297081a150ab3aa5b842be9b5792d849e2457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829116"
---
# <a name="mf_mt_mpeg2_content_packet-attribute"></a>Atributo de pacote de conteúdo do MF \_ MT \_ MPEG2 \_ \_

Para um tipo de mídia que descreve um fluxo de transporte MPEG-2 (TS), especifica se os pacotes de transporte contêm cabeçalhos de pacote de conteúdo.

## <a name="data-type"></a>Tipo de dados

**UINT32**



| Valor                                                                                                | Significado                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Nenhum cabeçalho de pacote de conteúdo é adicionado.<br/>                                                                                                                                                                    |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | A 200 a 1.000 intervalos de milissegundos, um cabeçalho de pacote de conteúdo de 14 bytes é adicionado ao início do pacote de transporte, conforme definido pela Associação de ARIB (setores de rádio e empresas) padrão.<br/> |



 

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

 

 




