---
description: Essas constantes são usadas em dois contextos.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: Constantes de LINEPROXYREQUEST_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755179"
---
# <a name="lineproxyrequest_-constants"></a>\_Constantes LINEPROXYREQUEST

Essas constantes são usadas em dois contextos. Primeiro, eles podem ser usados em uma matriz de valores **DWORD** na estrutura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passada com [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) quando a opção de \_ proxy LINEOPENOPTION é especificada, para indicar quais funções o aplicativo está disposto a lidar. Em segundo lugar, eles são usados na [**linha \_ PROXYREQUEST**](line-proxyrequest.md) passada para o aplicativo de manipulador por uma mensagem **\_ PROXYREQUEST de linha** para indicar o tipo de solicitação a ser processada e o formato dos dados no buffer.

<dl> <dt>

<span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**LINEPROXYREQUEST \_ AGENTSPECIFIC**
</dt> <dd> <dl> <dt>



Associado a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**CreateAgent do LINEPROXYREQUEST \_**
</dt> <dd> <dl> <dt>



Associado a [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**LINEPROXYREQUEST \_ CREATEAGENTSESSION**
</dt> <dd> <dl> <dt>



Associado a [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**LINEPROXYREQUEST \_ GETAGENTCAPS**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**LINEPROXYREQUEST \_ GETAGENTGROUPLIST**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**LINEPROXYREQUEST \_ GETAGENTINFO**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONINFO**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**LINEPROXYREQUEST \_ GETAGENTSESSIONLIST**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**LINEPROXYREQUEST \_ GETAGENTSTATUS**
</dt> <dd> <dl> <dt>



Associado a [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETgrouplist**
</dt> <dd> <dl> <dt>



Associado a [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**LINEPROXYREQUEST \_ GETQUEUEINFO**
</dt> <dd> <dl> <dt>



Associado a [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETqueuelist**
</dt> <dd> <dl> <dt>



Associado a [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**LINEPROXYREQUEST \_ SETAGENTACTIVITY**
</dt> <dd> <dl> <dt>



Associado a [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**LINEPROXYREQUEST \_ SETagent**
</dt> <dd> <dl> <dt>



Associado a [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD**
</dt> <dd> <dl> <dt>



Associado a [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE**
</dt> <dd> <dl> <dt>



Associado a [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**LINEPROXYREQUEST \_ SETagentstate**
</dt> <dd> <dl> <dt>



Associado a [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**LINEPROXYREQUEST \_ SETAGENTSTATEEX**
</dt> <dd> <dl> <dt>



Associado a [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD**
</dt> <dd> <dl> <dt>



Associado a [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de Call Center](call-center-constants.md)
</dt> <dt>

[Funções do Call Center](call-center-functions.md)
</dt> </dl>

 

 




