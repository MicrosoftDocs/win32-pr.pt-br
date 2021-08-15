---
title: MPENDOFLIFE_DATA estrutura (MpClient.h)
description: '\ 0034; Fim da vida útil \ 0034; dados de notificação.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA estrutura herdada Windows recursos de ambiente
- PMPENDOFLIFE_DATA de estrutura herdada Windows recursos de ambiente
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
ms.openlocfilehash: 532ee5f80e76de49c2c20bb01958e95fc13603b8f4b65666639834c5cad0fa72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476278"
---
# <a name="mpendoflife_data-structure"></a>Estrutura MPENDOFLIFE \_ DATA

Dados de notificação de "Fim da vida útil".

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

Tipo: **BOOL**

</dd> <dd>

True se o administrador controlar a política para mostrar a notificação. Se definido, isso informa à interface do usuário para não mostrar a notificação de EOL.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True se "Fim da vida útil" estiver pendente ou passado. Se for false, a interface do usuário e os clientes poderão limpar os estados relacionados ao EOL.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





