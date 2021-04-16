---
description: A \_ mensagem AGENTSTATUSEX de linha é enviada quando o status de um agente AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Mensagem de LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759049"
---
# <a name="line_agentstatusex-message"></a>Mensagem de AGENTSTATUSEX de linha \_

A **mensagem \_ AGENTSTATUSEX de linha** é enviada quando o status de um agente AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha. Isso está relacionado ao manipulador do agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

O identificador do agente cujo status foi alterado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica o status da fila que foi alterado. Pode ser uma ou mais das [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Se *dwParam2* incluir o \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indicará o novo valor do estado do agente, que é uma [**das \_ constantes LINEAGENTSTATEEX**](lineagentstateex--constants.md).

Caso contrário, *dwParam3* será definido como zero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




