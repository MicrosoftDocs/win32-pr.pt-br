---
title: Estrutura de MPSCAN_RESULT (MpClient. h)
description: Os resultados de uma verificação.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSCAN_RESULT
- Ponteiro de estrutura de PMPSCAN_RESULT recursos de ambiente herdados do Windows
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
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163623"
---
# <a name="mpscan_result-structure"></a>\_Estrutura de resultados MPSCAN

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

Tipo: **[ **\_ tipo de MPSCAN**](mpscan-type.md)**

</dd> <dd>

Tipo de verificação. Consulte [**\_ tipo de MPSCAN**](mpscan-type.md).

</dd> <dt>

**Origem**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

Verifique a origem, como o usuário ou o sistema iniciado. Consulte [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ScanGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

Identificador de verificação.

</dd> <dt>

**StartTime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Hora de início da verificação.

</dd> <dt>

**EndTime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Hora de término da verificação.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **\_ Estatísticas de MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estatísticas relacionadas a ameaças. Consulte [**\_ Estatísticas de MPTHREAT**](mpthreat-stats.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **\_ Estatísticas de MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Estatísticas relacionadas a recursos. Consulte [**\_ Estatísticas de MPRESOURCE**](mpresource-stats.md).

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estatísticas de MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**tipo de MPSCAN \_**](mpscan-type.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**Estatísticas de MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





