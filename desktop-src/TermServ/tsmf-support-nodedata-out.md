---
title: Estrutura de TSMF_SUPPORT_NODEDATA_OUT
description: Usado na estrutura de \_ saída de dados de suporte do TSMF \_ \_ para conter informações sobre formatos de mídia com suporte.
ms.assetid: cac0af9e-6750-4735-b075-46c77aea7d41
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_NODEDATA_OUT Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_NODEDATA_OUT Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_NODEDATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 517170e9d6580f69b59f71e0994351ebe0484ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824542"
---
# <a name="tsmf_support_nodedata_out-structure"></a>TSMF \_ dá suporte à \_ \_ estrutura de saída NODEDATA

Usado na estrutura [**de \_ \_ \_ saída de dados de suporte do TSMF**](tsmf-support-data-out.md) para conter informações sobre formatos de mídia com suporte.

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

**nodeId**
</dt> <dd>

O nó.

</dd> <dt>

**hrSupportStatus**
</dt> <dd>

Se o coletor identificado pelo parâmetro *clsidNewSink* tem suporte.

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

Outros valores são indefinidos.

</dd> <dt>

**clsidNewSink**
</dt> <dd>

O coletor associado ao tipo de mídia.

</dd> <dt>

**supportedMediaTypeIndex**
</dt> <dd>

O índice de base zero do tipo de mídia com suporte no coletor.

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

[**\_saída de \_ dados de suporte do TSMF \_**](tsmf-support-data-out.md)
</dt> </dl>

 

 





