---
description: As \_ constantes LINEAGENTSTATEEX descrevem o estado de um agente em um endereço.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Constantes de LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792616"
---
# <a name="lineagentstateex_-constants"></a>\_Constantes LINEAGENTSTATEEX

As **\_ constantes LINEAGENTSTATEEX** descrevem o estado de um agente em um endereço.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada roteada de uma fila AD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada de entrada que não foi transferida para o agente de uma fila ad na qual o agente está conectado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada de saída, como uma roteada de uma fila de discagem preditiva.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ ilegível**
</dt> <dd> <dl> <dt>



O agente está conectado, mas ocupado com uma tarefa que não atende a uma chamada (como em uma interrupção). Nenhuma chamada adicional deve ser roteada para o agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ pronto**
</dt> <dd> <dl> <dt>



O agente está pronto para aceitar chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ liberada**
</dt> <dd> <dl> <dt>



O agente foi liberado, provavelmente porque fez logoff.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ desconhecido**
</dt> <dd> <dl> <dt>



O estado do agente é desconhecido no momento, mas pode ser conhecido mais tarde. Esse pode ser um estado de transição quando uma linha ou um endereço é aberto pela primeira vez.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




