---
title: Estrutura de TSMF_SUPPORT_DATA_OUT
description: Contém informações sobre formatos de mídia. | Estrutura de TSMF_SUPPORT_DATA_OUT
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- Estrutura de TSMF_SUPPORT_DATA_OUT Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PTSMF_SUPPORT_DATA_OUT Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930314"
---
# <a name="tsmf_support_data_out-structure"></a>\_Estrutura de \_ saída de dados de suporte do TSMF \_

Contém informações sobre formatos de mídia. Essa estrutura é usada pelo método [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) durante consultas **de \_ \_ \_ \_ suporte ao formato MF de consulta WRDS** .

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

Isso deve corresponder à propriedade **guidMfSession** nos dados de [**suporte de TSMF correspondentes \_ \_ \_ na**](tsmf-support-data-in.md) estrutura.

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

[**TSMF \_ suporte \_ NODEDATA \_**](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





