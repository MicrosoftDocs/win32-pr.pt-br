---
title: MPCLEAN_DATA estrutura (MpClient.h)
description: Dados de notificação passados para a função de retorno de chamada limpa.
ms.assetid: 475A6525-5BD8-4B29-A684-53EE2758C790
keywords:
- MPCLEAN_DATA estrutura herdada Windows recursos de ambiente
- PMPCLEAN_DATA de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPCLEAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ece20324fc06fb68a813b374a698b2e27264068c9051bb2a5fff328c7ad328d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476334"
---
# <a name="mpclean_data-structure"></a>Estrutura MPCLEAN \_ DATA

Dados de notificação passados para a função de retorno de chamada limpa.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCLEAN_DATA {
  MPTHREAT_ID      ThreatID;
  MPTHREAT_ACTION  ThreatAction;
  DWORD            dwStatus;
  PMPRESOURCE_INFO ResourceInfo;
} MPCLEAN_DATA, *PMPCLEAN_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **\_ ID MPTHREAT**

</dd> <dd>

Identificador de ameaça para os eventos **MPNOTIFY \_ CLEAN \_ THREAT \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** O bit superior é definido para identificar ameaças relacionadas ao antivírus.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

Ação de ameaça para os **eventos MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Consulte [**MPTHREAT \_ ACTION**](mpthreat-action.md).

</dd> <dt>

**Dwstatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Status ou ações adicionais associadas à ação tomada. Essa é uma combinação de sinalizadores de bits do [**SINALIZADOR MPSTATUS \_**](mpstatus-flag.md).

</dd> <dt>

**ResourceInfo**
</dt> <dd>

Tipo: **PMPRESOURCE \_ INFO**

</dd> <dd>

Informações de recurso para os **eventos MPNOTIFY \_ CLEAN THREAT \_ \_ START** / **MPNOTIFY \_ CLEAN THREAT \_ \_ SUCCEEDED** / **MPNOTIFY \_ CLEAN THREAT \_ \_ FAILED.** Consulte [**INFORMAÇÕES DO MPRESOURCE. \_**](mpresource-info.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**INFORMAÇÕES DO MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**SINALIZADOR \_ MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**AÇÃO \_ MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





