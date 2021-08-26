---
title: TSMF_SUPPORT_DATA_OUT estrutura
description: Contém informações sobre formatos de mídia. | TSMF_SUPPORT_DATA_OUT estrutura
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT estrutura Serviços de Área de Trabalho Remota
- PTSMF_SUPPORT_DATA_OUT ponteiro de estrutura Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8577266c2e259e7a7e4bb70310837eee1d743905e0e0d166e5797bc51a1f1b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869016"
---
# <a name="tsmf_support_data_out-structure"></a>Estrutura TSMF \_ SUPPORT \_ DATA \_ OUT

Contém informações sobre formatos de mídia. Essa estrutura é usada pelo [**método QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante consultas **WRDS \_ QUERY \_ MF \_ FORMAT \_ SUPPORT.**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a>Membros

<dl> <dt>

**guidMfSession**
</dt> <dd>

Isso deve corresponder à **propriedade guidMfSession** na estrutura [**TSMF \_ SUPPORT DATA \_ \_ IN**](tsmf-support-data-in.md) correspondente.

</dd> <dt>

**numEntries**
</dt> <dd>

O número de estruturas nos dados de comprimento variável.

</dd> <dt>

**...**
</dt> <dd>

Um número variável de estruturas que contêm dados de formato de mídia.

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

[**NODEDATA OUT DE SUPORTE DO TSMF \_ \_ \_**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





