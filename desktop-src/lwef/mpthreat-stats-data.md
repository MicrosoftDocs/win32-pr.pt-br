---
title: Estrutura de MPTHREAT_STATS_DATA (MpClient. h)
description: Dados de estatísticas de ameaças adicionais.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_STATS_DATA
- Ponteiro de estrutura de PMPTHREAT_STATS_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085503"
---
# <a name="mpthreat_stats_data-structure"></a>Estrutura de dados de \_ estatísticas MPTHREAT \_

Dados de estatísticas de ameaças adicionais.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwThreatCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Número de ameaças.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





