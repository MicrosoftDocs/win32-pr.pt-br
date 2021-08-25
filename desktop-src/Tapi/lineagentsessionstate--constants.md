---
description: As constantes LINEAGENTSESSIONSTATE \_ descrevem vários estados de sessão do agente.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: LINEAGENTSESSIONSTATE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702c9820fb6c2157a386241b13ea0593c4156195bc74bcfa7655c76db171083d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682196"
---
# <a name="lineagentsessionstate_-constants"></a>Constantes LINEAGENTSESSIONSTATE \_

As **\_ constantes LINEAGENTSESSIONSTATE descrevem** vários estados de sessão do agente.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando a quebra da chamada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ ENCERRADO**
</dt> <dd> <dl> <dt>



A sessão do agente foi encerrada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NOTREADY**
</dt> <dd> <dl> <dt>



O agente está conectado, mas ocupado com uma tarefa diferente de atender a uma chamada (como em uma pausa). Nenhuma chamada adicional deve ser roteada para o agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ PRONTO**
</dt> <dd> <dl> <dt>



O agente está pronto para aceitar chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ LANÇADO**
</dt> <dd> <dl> <dt>



A sessão do agente foi liberada.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




