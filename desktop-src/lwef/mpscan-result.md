---
title: MPSCAN_RESULT (MpClient.h)
description: Os resultados de uma verificação.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- MPSCAN_RESULT estrutura herdada Windows recursos de ambiente
- PMPSCAN_RESULT de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a41efd40529976d4b7fe639c4907729ed39ae261f5ac644faf1a36e1a213a97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747147"
---
# <a name="mpscan_result-structure"></a>Estrutura MPSCAN \_ RESULT

Os resultados de uma verificação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a>Membros

<dl> <dt>

**ScanType**
</dt> <dd>

Tipo: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

</dd> <dd>

Tipo de verificação. Consulte [**MPSCAN \_ TYPE**](mpscan-type.md).

</dd> <dt>

**Origem**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Origem da verificação, como iniciado pelo usuário ou pelo sistema. Consulte [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Identificador de verificação.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Hora de início da verificação.

</dd> <dt>

**EndTime**
</dt> <dd>

Tipo: **ULARGE \_ INTEGER**

</dd> <dd>

Hora de término da verificação.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **ESTATÍSTICAS DE \_ MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estatísticas relacionadas a ameaças. Consulte [**ESTATÍSTICAS DE MPTHREAT \_**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **ESTATÍSTICAS de \_ MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Estatísticas relacionadas a recursos. Consulte [**ESTATÍSTICAS DO \_ MPRESOURCE.**](mpresource-stats.md)

</dd> <dt>

**SignatureVersion**
</dt> <dd>

Tipo: **ULONGLONG**

</dd> <dd>

Versão da assinatura usada para verificação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ESTATÍSTICAS DO MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**ESTATÍSTICAS DE \_ MPTHREAT**](mpthreat-stats.md)
</dt> </dl>

 

 





