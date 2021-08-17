---
description: As constantes LINEAGENTSTATEEX \_ descrevem o estado de um agente em um endereço.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: LINEAGENTSTATEEX_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f46c00b337a9106165616fe2eaf86bd2b2634b0c113369558953203313d59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140089"
---
# <a name="lineagentstateex_-constants"></a>Constantes LINEAGENTSTATEEX \_

As **\_ constantes LINEAGENTSTATEEX** descrevem o estado de um agente em um endereço.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada roteada de uma fila ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada de entrada que não foi transferida para o agente de uma fila ACD na qual o agente está conectado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada de saída, como uma roteada de uma fila de discagem preditiva.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NOTREADY**
</dt> <dd> <dl> <dt>



O agente está conectado, mas ocupado com uma tarefa diferente de atender a uma chamada (como em uma pausa). Nenhuma chamada adicional deve ser roteada para o agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ READY**
</dt> <dd> <dl> <dt>



O agente está pronto para aceitar chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ LANÇADO**
</dt> <dd> <dl> <dt>



O agente foi liberado, provavelmente porque foi desconectado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ UNKNOWN**
</dt> <dd> <dl> <dt>



O estado do agente é desconhecido no momento, mas pode se tornar conhecido posteriormente. Isso pode ser um estado de transição quando uma linha ou endereço é aberto pela primeira vez.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




