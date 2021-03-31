---
title: Estrutura de MPCOMPONENT_STATUS (MpClient. h)
description: Informações de status do componente.
ms.assetid: 0E589E52-A204-425C-880B-CF13C16893F3
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCOMPONENT_STATUS
- Ponteiro de estrutura de PMPCOMPONENT_STATUS recursos de ambiente herdados do Windows
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
ms.openlocfilehash: f2923136d2599440bc6ccfe863af9795f7d7ff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644530"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





