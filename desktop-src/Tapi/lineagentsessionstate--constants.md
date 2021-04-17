---
description: As \_ constantes LINEAGENTSESSIONSTATE descrevem vários Estados de sessão do agente.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Constantes de LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769408"
---
# <a name="lineagentsessionstate_-constants"></a>\_Constantes LINEAGENTSESSIONSTATE

As **\_ constantes LINEAGENTSESSIONSTATE** descrevem vários Estados de sessão do agente.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando uma chamada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**
</dt> <dd> <dl> <dt>



O agente está ocupado tratando o encapsulamento da chamada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ finalizado**
</dt> <dd> <dl> <dt>



A sessão do agente terminou.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ ilegível**
</dt> <dd> <dl> <dt>



O agente está conectado, mas ocupado com uma tarefa que não atende a uma chamada (como em uma interrupção). Nenhuma chamada adicional deve ser roteada para o agente.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ pronto**
</dt> <dd> <dl> <dt>



O agente está pronto para aceitar chamadas.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ liberada**
</dt> <dd> <dl> <dt>



A sessão do agente foi liberada.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




