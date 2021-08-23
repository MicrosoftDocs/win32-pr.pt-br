---
title: TSMF_SUPPORT_NODEDATA_OUT estrutura
description: Usado dentro da estrutura TSMF \_ SUPPORT DATA OUT para conter informações sobre \_ \_ formatos de mídia com suporte.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_NODEDATA_OUT estrutura Serviços de Área de Trabalho Remota
- PTSMF_SUPPORT_NODEDATA_OUT ponteiro de estrutura Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3eb4c515963e13d2a7919c58a6d55ca4b2a7600c429a33516093215b5ac0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869006"
---
# <a name="tsmf_support_nodedata_out-structure"></a>Estrutura \_ \_ NODEDATA OUT DE SUPORTE do TSMF \_

Usado dentro da estrutura [**TSMF \_ SUPPORT \_ DATA \_ OUT**](tsmf-support-data-out.md) para conter informações sobre formatos de mídia com suporte.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagTSMF_SUPPORT_NODEDATA_OUT {
  INT64   nodeId;
  HRESULT hrSupportStatus;
  CLSID   clsidNewSink;
  UINT32  supportedMediaTypeIndex;
} TSMF_SUPPORT_NODEDATA_OUT, *PTSMF_SUPPORT_NODEDATA_OUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Nodeid**
</dt> <dd>

O nó.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Se o sink identificado pelo parâmetro *clsidNewSink* tem suporte.

Os valores possíveis são.

<dt>

0
</dt> <dd>

Sem suporte

</dd> <dt>

1
</dt> <dd>

Com suporte

</dd> </dl>

Outros valores são indefinido.

</dd> <dt>

**clsidNewSink**
</dt> <dd>

O sink associado ao tipo de mídia.

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

O índice baseado em zero do tipo de mídia com suporte pelo sink.

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

[**DADOS DE SUPORTE DO TSMF \_ \_ \_ OUT**](tsmf-support-data-out.md)
</dt> </dl>

 

 





