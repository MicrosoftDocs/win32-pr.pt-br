---
title: Estrutura de MPCOMPONENT_STATUS (MpClient. h)
description: Informações de status do componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPCOMPONENT_STATUS
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPCOMPONENT_STATUS
topic_type:
- apiref
api_name:
- MPCOMPONENT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcb12a0358cf4d0112ca1cb8dfedc90c7c3aec504578685e78291dbe5e006cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747794"
---
# <a name="mpcomponent_status-structure"></a>Estrutura de status do MPCOMPONENT \_

Informações de status do componente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPCOMPONENT_STATUS {
  BOOL    fEnable;
  HRESULT hResult;
} MPCOMPONENT_STATUS, *PMPCOMPONENT_STATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**fEnable**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

Status do componente.

</dd> <dt>

**Resultado**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de êxito ou de falha associado ao status.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





