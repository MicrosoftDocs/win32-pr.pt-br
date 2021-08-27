---
title: MPHEALTH_DATA (MpClient.h)
description: Dados de notificação de saúde.
ms.assetid: 37A87F77-386A-4508-B338-ED2151518968
keywords:
- MPHEALTH_DATA estrutura herdada Windows recursos de ambiente
- PMPHEALTH_DATA de estrutura herdada Windows recursos de ambiente
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
ms.openlocfilehash: cb04224d38e639d053b8e20370e2b0db0dc15f44cc647e7205911362112e4a49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975996"
---
# <a name="mphealth_data-structure"></a>Estrutura MPHEALTH \_ DATA

Dados de notificação de saúde.

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
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





