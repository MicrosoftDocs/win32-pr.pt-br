---
title: Estrutura de MPENDOFLIFE_DATA (MpClient. h)
description: '\ 0034; Fim da vida útil \ 0034; dados de notificação.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPENDOFLIFE_DATA
- Ponteiro de estrutura de PMPENDOFLIFE_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085946"
---
# <a name="mpendoflife_data-structure"></a>\_Estrutura de dados MPENDOFLIFE

Dados de notificação "fim da vida útil".

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**ftSignatureExpiry**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

Hora em que a assinatura expira.

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

Hora em que a plataforma expira.

</dd> <dt>

**fAdminControlled**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se o administrador que controla a política para mostrar a notificação. Se definido, isso informa a interface do usuário para não mostrar a notificação de EOL.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se "End of Life" estiver pendente ou passado. Se false, a interface do usuário e os clientes podem limpar quaisquer Estados relacionados a EOL.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





