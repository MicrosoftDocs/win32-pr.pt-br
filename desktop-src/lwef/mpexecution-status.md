---
title: Enumeração de MPEXECUTION_STATUS (MpClient. h)
description: Possível status de execução de ameaça.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPEXECUTION_STATUS
- PMPEXECUTION_STATUS recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824306"
---
# <a name="mpexecution_status-enumeration"></a>\_Enumeração de status MPEXECUTION

Possível status de execução de ameaça.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**STATUS de execução do MP \_ \_ \_ desconhecido**
</dt> <dd>

O status de execução não é conhecido.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**STATUS de execução do MP \_ \_ \_ bloqueado**
</dt> <dd>

Bloqueado da execução por mini-Filter.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**STATUS de execução do MP \_ \_ \_ permitido**
</dt> <dd>

Permissão para executar por mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**execuções do status de execução do MP \_ \_ \_**
</dt> <dd>

A ameaça está em execução.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**o status de execução do MP não está em \_ \_ \_ \_ execução**
</dt> <dd>

A ameaça não está em execução e só está disponível no mecanismo durante a correção.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





