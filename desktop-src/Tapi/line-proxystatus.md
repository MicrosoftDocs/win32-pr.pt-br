---
description: A mensagem LINE PROXYSTATUS é enviada quando os proxies disponíveis mudam em uma linha que o \_ aplicativo tem aberto no momento.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: LINE_PROXYSTATUS mensagem (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585feda6194a13ecfbe17292aadb9036784d244c9ee5b7df4361981ab7401f65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682346"
---
# <a name="line_proxystatus-message"></a>Mensagem \_ LINE PROXYSTATUS

A **mensagem \_ LINE PROXYSTATUS** é enviada quando os proxies disponíveis mudam em uma linha que o aplicativo tem aberto no momento.

TAPISRV gera essa mensagem durante uma função [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) usando LINEPROXYSTATUS OPEN e \_ \_ LINEPROXYSTATUS ALLOPENFORACD ou uma função [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) usando LINEPROXYSTATUS CLOSE (todas as \_ [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md)).


```C++
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwDevice* 
</dt> <dd>

O alça do aplicativo para o dispositivo de linha. Isso está relacionado ao manipulador de agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

A instância de retorno de chamada fornecida ao abrir a linha.

</dd> <dt>

*Dwparam1* 
</dt> <dd>

Especifica o status da fila que foi alterado. Pode ser uma ou mais das [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md).

</dd> <dt>

*Dwparam2* 
</dt> <dd>

Se *dwParam1* for definido como LINEPROXYSTATUS OPEN ou \_ LINEPROXYSTATUS \_ CLOSE, *dwParam2* indicará o tipo de solicitação de proxy relacionado, que é um dos seguintes:

-   LINEPROXYREQUEST \_ SETAGENTGROUP
-   LINEPROXYREQUEST \_ SETAGENTSTATE
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   LINEPROXYREQUEST \_ CREATEAGENT
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETQUEUELIST
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETGROUPLIST
-   LINEPROXYREQUEST \_ SETAGENTSTATEEX

Caso contrário, *dwParam2* será definido como zero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Definido como zero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 2.2<br/>                                                      |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lineopen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**Lineclose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**LINE \_ PROXYREQUEST**](line-proxyrequest.md)
</dt> <dt>

[**Constantes LINEPROXYREQUEST \_**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




