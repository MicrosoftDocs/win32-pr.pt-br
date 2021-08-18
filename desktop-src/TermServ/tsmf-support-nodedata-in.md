---
title: TSMF_SUPPORT_NODEDATA_IN estrutura
description: Usado dentro da estrutura TSMF \_ SUPPORT DATA IN para conter informações sobre \_ \_ formatos de mídia com suporte.
ms.assetid: 9aee9d6d-2182-44ec-ba8b-d2747d3edf71
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_IN estrutura Serviços de Área de Trabalho Remota
- PTSMF_SUPPORT_NODEDATA_IN ponteiro de estrutura Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e1920ca627a7da8aef2d49a6930b03f0906cfd912e2a2a584b20d8e8382b706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755718"
---
# <a name="tsmf_support_nodedata_in-structure"></a>ESTRUTURA TSMF \_ SUPPORT \_ NODEDATA \_ IN

Usado dentro da estrutura [**TSMF \_ SUPPORT \_ DATA \_ IN**](tsmf-support-data-in.md) para conter informações sobre formatos de mídia com suporte.

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

**Bytecount**
</dt> <dd>

O tamanho da estrutura em bytes.

</dd> <dt>

**Nodeid**
</dt> <dd>

O nó.

</dd> <dt>

**numMediaTypes**
</dt> <dd>

O número de estruturas de formato de mídia.

</dd> <dt>

**...**
</dt> <dd>

Um número variável de estruturas que definem formatos de mídia de áudio ou vídeo. FormatType **é** **FORMAT \_ WaveFormatEx para** áudio ou **FORMAT \_ MFVideoFormat** para vídeo.

Para obter detalhes dessa estrutura, consulte Estrutura de tipo de [mídia TS \_ AM \_ \_ ](/openspecs/windows_protocols/ms-rdpev/22a57950-042e-48bd-8135-3580f3a3f934).

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

[**DADOS DE SUPORTE DO TSMF \_ \_ \_ NO**](tsmf-support-data-in.md)
</dt> </dl>

 

