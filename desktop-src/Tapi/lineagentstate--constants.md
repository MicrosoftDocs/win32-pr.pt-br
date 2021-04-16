---
description: As \_ constantes LINEAGENTSTATE descrevem o estado de um agente em um endereço.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Constantes de LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757618"
---
# <a name="lineagentstate_-constants"></a>\_Constantes LINEAGENTSTATE

As **\_ constantes LINEAGENTSTATE** descrevem o estado de um agente em um endereço.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada roteada de uma fila AD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada de entrada que não foi transferida para o agente de uma fila ad na qual o agente está conectado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**
</dt> <dd> <dl> <dt>



O agente está ocupado lidando com outro tipo de chamada, como uma chamada pessoal de saída não transferida para o agente por uma discagem preditiva. Esse valor também pode ser usado quando o agente é conhecido como ocupado em uma chamada, mas o tipo de chamada é desconhecido.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada de saída, como uma roteada de uma fila de discagem preditiva.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**
</dt> <dd> <dl> <dt>



Nenhum agente está conectado no endereço.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ ilegível**
</dt> <dd> <dl> <dt>



O agente está conectado, mas ocupado com uma tarefa que não atende a uma chamada (como em uma interrupção). Nenhuma chamada adicional deve ser roteada para o agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ pronto**
</dt> <dd> <dl> <dt>



O agente está pronto para aceitar chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE não \_ disp.**
</dt> <dd> <dl> <dt>



O estado do agente é desconhecido e nunca se tornará conhecido. No [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), essa condição também pode ser representada pelo membro **dwAgentState** que está sendo definido como 0.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ desconhecido**
</dt> <dd> <dl> <dt>



O estado do agente é desconhecido no momento, mas pode ser conhecido mais tarde. Esse pode ser um estado de transição quando uma linha ou um endereço é aberto pela primeira vez.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**
</dt> <dd> <dl> <dt>



O agente concluiu a chamada anterior, mas ainda está ocupado com o trabalho relacionado a essa chamada. O agente não deve receber chamadas adicionais.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Os 16 bits superiores deste conjunto de constantes são reservados para extensões específicas do dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




