---
title: Estrutura de MPTHREAT_STATS (MpClient. h)
description: Estatísticas relacionadas a ameaças.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPTHREAT_STATS
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPTHREAT_STATS
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7671b45dc09c8aca494ad270aa69fc386ef3d7c03d5144fdc3e89b4f657bb07b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975936"
---
# <a name="mpthreat_stats-structure"></a>\_Estrutura de estatísticas MPTHREAT

Estatísticas relacionadas a ameaças.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a>Membros

<dl> <dt>

**ThreatCount**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Número de ameaças detectadas.

</dd> <dt>

**SuspiciousThreatCount**
</dt> <dd>

Tipo: **uint**

</dd> <dd>

Número de ameaças detectadas com monitoramento de comportamento.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **uint \[ 4 \]**

</dd> <dd>

Campos reservados para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





