---
title: Estrutura de MPNIS_PRIVATE_DATA (MpClient. h)
description: Notificações NIS privadas.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPNIS_PRIVATE_DATA
- Ponteiro de estrutura de PMPNIS_PRIVATE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644309"
---
# <a name="mpnis_private_data-structure"></a>\_Estrutura de dados privada do MPNIS \_

Notificações NIS privadas.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo de notificação.

</dd> <dt>

**cbDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tamanho dos dados reservados, em bytes.

</dd> <dt>

**pbData**
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



 

 





