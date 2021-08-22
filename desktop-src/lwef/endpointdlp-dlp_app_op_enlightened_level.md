---
description: Associa uma ação DLP (Prevenção contra Perda de Dados) do ponto de extremidade a um nível de imposição.
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
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL estrutura

Associa uma ação DLP (Prevenção contra Perda de Dados) do ponto de extremidade a um nível de imposição.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Membros

<dl> <dt>

*Operação* \[ Em\]
</dt> <dd>

Um valor da [enumeração DlpActionType que](endpointdlp-dlpactiontype.md) especifica o tipo de ação DLP do ponto de extremidade.

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[ Em\]
</dt> <dd>

Um valor do [DlpAppEnforceLevel que](endpointdlp-dlpappenforcelevel.md) especifica o nível de imposição para o tipo de ação DLP do ponto de extremidade associado.

</dd> </dl>





## <a name="remarks"></a>Comentários

Passe uma matriz dessas estruturas para [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) para definir o modo de imposição para um conjunto de operações DLP de ponto de extremidade.

## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |

