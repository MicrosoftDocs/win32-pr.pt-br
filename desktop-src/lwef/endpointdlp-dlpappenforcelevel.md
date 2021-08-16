---
description: Especifica o nível de imposição de uma operação DLP (Prevenção contra Perda de Dados) do ponto de extremidade.
title: Enumeração DlpAppEnforceLevel (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 99bd06a41c88ff0b5a02b9b329877c015aea7dfb3fdbc58fea3c2e305829faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349346"
---
# <a name="dlpappenforcelevel-enumeration"></a>Enumeração DlpAppEnforceLevel

Especifica o nível de imposição de uma operação DLP (Prevenção contra Perda de Dados) do ponto de extremidade.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>Constantes

<dl> <dt>

*DlpAppEnforceLevelNone* \[ Em\]
</dt> <dd>

Nenhuma imposição pelo aplicativo. O sistema DLP imporá a operação.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[ Em\]
</dt> <dd>

O aplicativo Tne usará as APIs DLP para notificar o sistema DLP sobre a operação. O sistema DLP imporá a operação.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[ Em\]
</dt> <dd>

Sem suporte na versão atual.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[ Em\]
</dt> <dd>

Sem suporte na versão atual.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[ Em\]
</dt> <dd>

O valor máximo da enumeração.

</dd> </dl>



## <a name="remarks"></a>Comentários

Os valores dessa enumeração são usados pela [estrutura DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) dados.


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |

