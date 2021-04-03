---
title: Estrutura de MPSTATUS_INFO (MpClient. h)
description: Informações de status do Malware Protection Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSTATUS_INFO
- Ponteiro de estrutura de PMPSTATUS_INFO recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644307"
---
# <a name="mpstatus_info-structure"></a>Estrutura de informações do MPSTATUS \_

Informações de status do Malware Protection Manager.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**ProductStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Status geral do produto. Essa é uma combinação de sinalizadores de bit [**do \_ sinalizador MPSTATUS**](mpstatus-flag.md).

</dd> <dt>

**LastQuickScan**
</dt> <dd>

Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**

</dd> <dd>

Resultados da última verificação pelo Gerenciador de proteção contra malware. Consulte [**\_ resultado do MPSCAN**](mpscan-result.md).

</dd> <dt>

**LastFullScan**
</dt> <dd>

Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**

</dd> <dd>

Resultados da última verificação completa pelo Malware Protection Manager. Consulte [**\_ resultado do MPSCAN**](mpscan-result.md).

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **\_ Estatísticas de MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estatísticas de ameaça ativas. Consulte [**\_ Estatísticas de MPTHREAT**](mpthreat-stats.md).

</dd> <dt>

**Threatstate**
</dt> <dd>

Tipo: **[**MPTHREAT \_ estatísticas \_ dados**](mpthreat-stats-data.md) \[ MP \_ ameaça \_ \_ máximo \_ valor + 1\]**

</dd> <dd>

Dados de estatísticas de ameaças adicionais, como o número de ameaças. Consulte [**\_ \_ dados de estatísticas do MPTHREAT**](mpthreat-stats-data.md).

</dd> <dt>

**Componente**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ status**](mpcomponent-status.md) \[ MPCOMPONENT \_ MaxValue + 1\]**

</dd> <dd>

Uma matriz de status para vários componentes. Use um valor da enumeração [**de \_ ID MPCOMPONENT**](mpcomponent-id.md) como um índice na matriz.

</dd> <dt>

**ProductExpirationTime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Carimbo de data/hora de validade do produto em UNC. Isso será válido somente se o status de expiração for definido.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID do MPCOMPONENT \_**](mpcomponent-id.md)
</dt> <dt>

[**STATUS do MPCOMPONENT \_**](mpcomponent-status.md)
</dt> <dt>

[**resultado do MPSCAN \_**](mpscan-result.md)
</dt> <dt>

[**\_sinalizador MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**Estatísticas de MPTHREAT \_**](mpthreat-stats.md)
</dt> <dt>

[**\_dados de estatísticas do MPTHREAT \_**](mpthreat-stats-data.md)
</dt> </dl>

 

 





