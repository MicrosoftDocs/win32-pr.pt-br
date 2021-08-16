---
description: Associa uma ação de DLP (prevenção de perda de dados) de ponto de extremidade com um nível de imposição.
title: Estrutura DLP_APP_OP_ENLIGHTENED_LEVEL (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e47fa7705701701af2fc0832c5ea27cfdc7d1e67948ec095f3c24837a93de18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610476"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>Estrutura de DLP_APP_OP_ENLIGHTENED_LEVEL

Associa uma ação de DLP (prevenção de perda de dados) de ponto de extremidade com um nível de imposição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Membros

<dl> <dt>

*Operação* \[ do no\]
</dt> <dd>

Um valor da enumeração [DlpActionType](endpointdlp-dlpactiontype.md) especificando o tipo de ação de DLP do ponto de extremidade.

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[ no\]
</dt> <dd>

Um valor de [DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md) que especifica o nível de imposição para o tipo de ação de DLP de ponto de extremidade associado.

</dd> </dl>





## <a name="remarks"></a>Comentários

Passe uma matriz dessas estruturas em [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) para definir o modo de imposição para um conjunto de operações de DLP de ponto de extremidade.

## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |

