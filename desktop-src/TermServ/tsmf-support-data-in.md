---
title: Estrutura de TSMF_SUPPORT_DATA_IN
description: Contém informações sobre formatos de mídia. | Estrutura de TSMF_SUPPORT_DATA_IN
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_DATA_IN Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_DATA_IN Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ae90099b69494425344ff65b73090cce574b843cd1589572203a4786b38ff6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755772"
---
# <a name="tsmf_support_data_in-structure"></a>\_ \_ Dados de suporte \_ do TSMF na estrutura

Contém informações sobre formatos de mídia. Essa estrutura é usada pelo método [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante consultas **de \_ \_ \_ \_ suporte ao formato MF de consulta WRDS** .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a>Membros

<dl> <dt>

**guidMfSession**
</dt> <dd>

A sessão.

</dd> <dt>

**numEntries**
</dt> <dd>

O número de estruturas nos dados de comprimento variável.

</dd> <dt>

**...**
</dt> <dd>

Um número variável de estruturas que contém dados de formato de mídia.

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

[**TSMF \_ suportam \_ NODEDATA \_**](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





