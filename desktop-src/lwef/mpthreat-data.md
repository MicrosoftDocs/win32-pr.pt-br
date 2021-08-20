---
title: Estrutura de MPTHREAT_DATA (MpClient. h)
description: Dados de notificação passados devido a uma detecção de ameaças ou modificação.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPTHREAT_DATA
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPTHREAT_DATA
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
ms.openlocfilehash: 2bd6338a027e3b03971f357950bbc351acef0d3fcdca83b72130e0ea475164d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883226"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_sinalizador MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_ação MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





