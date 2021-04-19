---
description: Especifica o nível de imposição de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.
title: Enumeração DlpAppEnforceLevel (endpointdlp. h)
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
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495361"
---
# <a name="dlpappenforcelevel-enumeration"></a>Enumeração DlpAppEnforceLevel

Especifica o nível de imposição de uma operação de DLP (prevenção de perda de dados) de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


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

*DlpAppEnforceLevelNone* \[ no\]
</dt> <dd>

Nenhuma imposição pelo aplicativo. O sistema DLP irá impor a operação.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[ no\]
</dt> <dd>

O aplicativo TNE usará as APIs DLP para notificar o sistema DLP sobre a operação. O sistema DLP irá impor a operação.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[ no\]
</dt> <dd>

Sem suporte na versão atual.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[ no\]
</dt> <dd>

Sem suporte na versão atual.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[ no\]
</dt> <dd>

O valor máximo da enumeração.

</dd> </dl>



## <a name="remarks"></a>Comentários

Os valores dessa enumeração são usados pela estrutura de [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) .


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |

