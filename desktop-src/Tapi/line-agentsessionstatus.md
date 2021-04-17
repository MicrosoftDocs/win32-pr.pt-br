---
description: A mensagem de linha \_ AGENTSESSIONSTATUS é enviada quando o status de uma sessão de agente AD é alterado em um manipulador de agente para o qual o aplicativo tem atualmente uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Mensagem de LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761356"
---
# <a name="line_agentsessionstatus-message"></a>Mensagem de AGENTSESSIONSTATUS de linha \_

A mensagem de **linha \_ AGENTSESSIONSTATUS** é enviada quando o status de uma sessão de agente AD é alterado em um manipulador de agente para o qual o aplicativo tem atualmente uma linha aberta. Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .


```C++
        
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

O identificador do aplicativo para o dispositivo de linha no qual o status da sessão do agente foi alterado.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Um identificador da sessão do agente cujo status foi alterado.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Especifica o status de sessão do agente que foi alterado. Pode ser uma ou mais das **\_ AGENTSESSIONSTATUS de linha**.

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

[**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




