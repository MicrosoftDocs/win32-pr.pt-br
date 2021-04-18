---
title: Estrutura de TSMF_SUPPORT_NODEDATA_IN
description: Usado dentro dos dados de suporte do TSMF \_ \_ \_ na estrutura para conter informações sobre formatos de mídia com suporte.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_NODEDATA_IN Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_NODEDATA_IN Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c36d18ea0e97da8df60475855c93755727fa87d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105796294"
---
# <a name="tsmf_support_nodedata_in-structure"></a>TSMF \_ dá suporte a \_ NODEDATA \_ na estrutura

Usado dentro dos [**dados de suporte do TSMF \_ \_ \_ na**](tsmf-support-data-in.md) estrutura para conter informações sobre formatos de mídia com suporte.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_IN {
  UINT32           byteCount;
  INT64            nodeId;
  UINT32           numMediaTypes;
  TS_AM_MEDIA_TYPE ...;
} TSMF_SUPPORT_NODEDATA_IN, *PTSMF_SUPPORT_NODEDATA_IN;
```



## <a name="members"></a>Membros

<dl> <dt>

**byteCount**
</dt> <dd>

O tamanho da estrutura em bytes.

</dd> <dt>

**nodeId**
</dt> <dd>

O nó.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

O número de estruturas de formato de mídia.

</dd> <dt>

**...**
</dt> <dd>

Um número variável de estruturas que definem formatos de mídia de áudio ou vídeo. O **formatType** é o **formato \_ WaveFormatEx** para áudio ou **formato \_ MFVideoFormat** para vídeo.

Para obter detalhes dessa estrutura, consulte [ \_ estrutura do \_ \_ tipo de mídia TS am](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>         |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[**\_ \_ dados de suporte \_ do TSMF em**](tsmf-support-data-in.md)
</dt> </dl>

 

