---
title: Estrutura de MPHEALTH_DATA (MpClient. h)
description: Dados de notificação de integridade.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPHEALTH_DATA
- Ponteiro de estrutura de PMPHEALTH_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPHEALTH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e729bdea82b6a885b64e95ecd77f9deae6bff4e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105797907"
---
# <a name="mphealth_data-structure"></a>\_Estrutura de dados MPHEALTH

Dados de notificação de integridade.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPHEALTH_DATA {
  DWORD dwNotificationType;
  DWORD dwNotificationFlag;
} MPHEALTH_DATA, *PMPHEALTH_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo de notificação.

</dd> <dt>

**dwNotificationFlag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Não utilizado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





