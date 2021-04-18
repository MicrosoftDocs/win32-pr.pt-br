---
title: Estrutura de MPTHREAT_DATA (MpClient. h)
description: Dados de notificação passados devido a uma detecção de ameaças ou modificação.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_DATA
- Ponteiro de estrutura de PMPTHREAT_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787665"
---
# <a name="mpthreat_data-structure"></a>\_Estrutura de dados MPTHREAT

Dados de notificação passados devido a uma detecção de ameaças ou modificação.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Threatid**
</dt> <dd>

Tipo: **\_ ID de MPTHREAT**

</dd> <dd>

Identificador de ameaça. O bit superior é definido para identificar ameaças relacionadas ao antivírus.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sessão associada à ameaça. Defina como-1 se nenhuma informação específica de sessão estiver disponível.

</dd> <dt>

**Threataction**
</dt> <dd>

Tipo: **[ **\_ ação MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Ação de ameaça tentada para a **\_ limpeza de ameaça mpnotify \_ \_ bem-sucedida** / **mpnotify eventos \_ \_ \_ com falha na limpeza de ameaças** .

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Status ou ações adicionais associadas à ação executada. Essa é uma combinação de sinalizadores de bit [**do \_ sinalizador MPSTATUS**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_sinalizador MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_ação MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





