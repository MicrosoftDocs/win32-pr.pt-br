---
title: MPRESERVED_DATA (MpClient.h)
description: Dados de notificação reservados.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA estrutura herdada Windows recursos de ambiente
- PMPRESERVED_DATA de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747650"
---
# <a name="mpreserved_data-structure"></a>Estrutura MPRESERVED \_ DATA

Dados de notificação reservados.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbReservedData**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamanho dos dados reservados, em bytes.

</dd> <dt>

**pbReservedData**
</dt> <dd>

Tipo: **BYTE \***

</dd> <dd>

Ponteiro para dados reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





