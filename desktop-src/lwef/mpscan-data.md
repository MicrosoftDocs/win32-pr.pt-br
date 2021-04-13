---
title: Estrutura de MPSCAN_DATA (MpClient. h)
description: Verifique os dados passados para o retorno de chamada.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSCAN_DATA
- Ponteiro de estrutura de PMPSCAN_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455963"
---
# <a name="mpscan_data-structure"></a>\_Estrutura de dados MPSCAN

Verifique os dados passados para o retorno de chamada.

Essa estrutura contém as estatísticas de recursos e ameaças cumulativas. Esses campos de estatística são sempre válidos.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**ScanType**
</dt> <dd>

Tipo: **[ **\_ tipo de MPSCAN**](mpscan-type.md)**

</dd> <dd>

Tipo de verificação.

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **\_ informações de PMPRESOURCE**

</dd> <dd>

Informações sobre o recurso. Consulte [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**ResourceStats**
</dt> <dd>

Tipo: **[ **\_ Estatísticas de MPRESOURCE**](mpresource-stats.md)**

</dd> <dd>

Estatísticas cumulativas relacionadas a recursos.

</dd> <dt>

**ThreatStats**
</dt> <dd>

Tipo: **[ **\_ Estatísticas de MPTHREAT**](mpthreat-stats.md)**

</dd> <dd>

Estatísticas de ameaças com conclusões de verificação bem-sucedidas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**Estatísticas de MPRESOURCE \_**](mpresource-stats.md)
</dt> <dt>

[**tipo de MPSCAN \_**](mpscan-type.md)
</dt> <dt>

[**Estatísticas de MPTHREAT \_**](mpthreat-stats.md)
</dt> </dl>

 

 





