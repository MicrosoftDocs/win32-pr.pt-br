---
description: A mensagem de linha \_ PROXYSTATUS é enviada quando os proxies disponíveis são alterados em uma linha que o aplicativo abriu atualmente.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Mensagem de LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753343"
---
# <a name="line_proxystatus-message"></a>Mensagem de PROXYSTATUS de linha \_

A mensagem de **linha \_ PROXYSTATUS** é enviada quando os proxies disponíveis são alterados em uma linha que o aplicativo abriu atualmente.

TAPISRV gera essa mensagem durante uma função [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) usando LINEPROXYSTATUS \_ Open e LINEPROXYSTATUS \_ ALLOPENFORACD ou uma função [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) usando LINEPROXYSTATUS \_ Close (todas as [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md)).


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

Especifica o status da fila que foi alterado. Pode ser uma ou mais das [**\_ constantes LINEPROXYSTATUS**](lineproxystatus--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Se *dwParam1* for definido como LINEPROXYSTATUS \_ Open ou LINEPROXYSTATUS \_ Close, *dwParam2* indicará o tipo de solicitação de proxy relacionado, que é um dos seguintes:

-   LINEPROXYREQUEST \_ SETagent
-   LINEPROXYREQUEST \_ SETagentstate
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   CreateAgent do LINEPROXYREQUEST \_
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETqueuelist
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETgrouplist
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
| Versão da TAPI<br/> | Requer TAPI 2,2<br/>                                                      |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**PROXYREQUEST de linha \_**](line-proxyrequest.md)
</dt> <dt>

[**\_Constantes LINEPROXYREQUEST**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




