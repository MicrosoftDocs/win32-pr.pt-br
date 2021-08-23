---
description: Descreve o conteúdo de um fluxo elementar dentro de um fluxo de transporte MPEG-2. Essa enumeração é usada na interface IMPEG2PIDMap, que é implementada nos pinos de saída do demultiplexador MPEG-2.
ms.assetid: 989ad56b-b5af-4811-889e-c79fcd3f7f01
title: Enumeração de MEDIA_SAMPLE_CONTENT (Bdatypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SAMPLE_CONTENT
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: 1dead22b2c8ea3cf7da665e01a4b36554b8282922a1d2b2a12d59f429f2acac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684986"
---
# <a name="media_sample_content-enumeration"></a>Enumeração de conteúdo de \_ exemplo de mídia \_

Descreve o conteúdo de um fluxo elementar dentro de um fluxo de transporte MPEG-2. Essa enumeração é usada na interface [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap) , que é implementada nos pinos de saída do [demultiplexador MPEG-2](mpeg-2-demultiplexer.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MEDIA_TRANSPORT_PACKET,
  MEDIA_ELEMENTARY_STREAM,
  MEDIA_MPEG2_PSI,
  MEDIA_TRANSPORT_PAYLOAD
} MEDIA_SAMPLE_CONTENT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MEDIA_TRANSPORT_PACKET"></span><span id="media_transport_packet"></span>**\_pacote de transporte de mídia \_**
</dt> <dd>

Especifica um pacote de fluxo de transporte completo a ser passado sem processamento.

</dd> <dt>

<span id="MEDIA_ELEMENTARY_STREAM"></span><span id="media_elementary_stream"></span>**\_fluxo elementar mídia \_**
</dt> <dd>

Especifica uma carga de áudio/vídeo PES.

</dd> <dt>

<span id="MEDIA_MPEG2_PSI"></span><span id="media_mpeg2_psi"></span>**MPEG2 de mídia \_ \_ psi**
</dt> <dd>

Especifica um fluxo de dados PAT, pgto, CAT ou Private. Essas são seções completas do PSI que não precisam ser remontadas.

</dd> <dt>

<span id="MEDIA_TRANSPORT_PAYLOAD"></span><span id="media_transport_payload"></span>**\_carga de transporte de mídia \_**
</dt> <dd>

Especifica cargas de pacotes TS coletadas, como pacotes PES.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Bdatypes. h (incluir Bdaiface. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[DirectShow Tipos enumerados](directshow-enumerated-types.md)
</dt> </dl>

 

 




