---
title: Estrutura de MPRESERVED_DATA (MpClient. h)
description: Dados de notificação reservados.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPRESERVED_DATA
- Ponteiro de estrutura de PMPRESERVED_DATA recursos de ambiente herdados do Windows
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
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085845"
---
# <a name="mpreserved_data-structure"></a>\_Estrutura de dados MPRESERVED

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

Tipo: **byte \***

</dd> <dd>

Ponteiro para dados reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





