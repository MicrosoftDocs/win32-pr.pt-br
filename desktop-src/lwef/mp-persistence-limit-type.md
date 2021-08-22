---
title: MP_PERSISTENCE_LIMIT_TYPE enumeração (MpClient.h)
description: Tipo de limite de persistência.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- MP_PERSISTENCE_LIMIT_TYPE de enumeração herdada Windows recursos de ambiente
- PMP_PERSISTENCE_LIMIT_TYPE de enumeração herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2a56d4962467abe0ad338af257aca2581e612c100468fbdf2853aa4d71290ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608996"
---
# <a name="mp_persistence_limit_type-enumeration"></a>\_Enumeração MP PERSISTENCE \_ LIMIT \_ TYPE

Tipo de limite de persistência.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**PERSISTÊNCIA DE MP \_ \_ DESCONHECIDA**
</dt> <dd>

Desconhecido.

</dd> <dt>

<span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**PERSISTÊNCIA DE MP \_ \_ SEM \_ LIMITE**
</dt> <dd>

Não há limite.

</dd> <dt>

<span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**DURAÇÃO \_ DA PERSISTÊNCIA DO \_ MP**
</dt> <dd>

Duração.

</dd> <dt>

<span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**VERSÃO \_ DA \_ VDM DE PERSISTÊNCIA \_ DO MP**
</dt> <dd>

Versão da VDM.

</dd> <dt>

<span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP \_ PERSISTENCE \_ TIMESTAMP**
</dt> <dd>

Timestamp.

</dd> <dt>

<span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**PERSISTÊNCIA DE MP \_ \_ FORÇADA**
</dt> <dd>

Forçado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





