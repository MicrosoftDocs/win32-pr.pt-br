---
title: Estrutura de MPTHREAT_STATS (MpClient. h)
description: Estatísticas relacionadas a ameaças.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_STATS
- Ponteiro de estrutura de PMPTHREAT_STATS recursos de ambiente herdados do Windows
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
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824372"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





