---
title: MPEXECUTION_STATUS enumeração (MpClient.h)
description: Possível status de execução de ameaças.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- MPEXECUTION_STATUS de enumeração herdada Windows recursos de ambiente
- PMPEXECUTION_STATUS de enumeração herdado Windows recursos de ambiente
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
ms.openlocfilehash: 6e4748b6d97e1b7ee05db8044837b89e2653a14fd1e6f87068a40107cdd9ee60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943906"
---
# <a name="mpexecution_status-enumeration"></a>Enumeração MPEXECUTION \_ STATUS

Possível status de execução de ameaças.

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

<span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**STATUS \_ DE EXECUÇÃO DO MP \_ \_ DESCONHECIDO**
</dt> <dd>

O status de execução não é conhecido.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**STATUS \_ DE EXECUÇÃO DO MP \_ \_ BLOQUEADO**
</dt> <dd>

Bloqueado da execução por mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**STATUS \_ DE EXECUÇÃO DO MP \_ \_ PERMITIDO**
</dt> <dd>

Permissão para executar por mini-filtro.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**STATUS \_ DE EXECUÇÃO DO MP EM \_ \_ EXECUÇÃO**
</dt> <dd>

A ameaça está em execução.

</dd> <dt>

<span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**STATUS \_ DE EXECUÇÃO DO MP NÃO EM \_ \_ \_ EXECUÇÃO**
</dt> <dd>

A ameaça não está em execução e só está disponível no mecanismo durante a correção.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





