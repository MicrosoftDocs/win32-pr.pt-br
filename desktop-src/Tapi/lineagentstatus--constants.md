---
description: As \_ constantes LINEAGENTSTATUS listam o status de atualização dos membros da estrutura LINEAGENTSTATUS para um agente.
ms.assetid: 068a2b24-a430-4cf5-b70d-5574e981a899
title: Constantes de LINEAGENTSTATUS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1fb7afb2703a50d97d0423662a10c92743beb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764759"
---
# <a name="lineagentstatus_-constants"></a>\_Constantes LINEAGENTSTATUS

As **\_ constantes LINEAGENTSTATUS** listam o status de atualização dos membros da estrutura [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) para um agente.

<dl> <dt>

<span id="LINEAGENTSTATUS_ACTIVITY"></span><span id="lineagentstatus_activity"></span>**\_atividade LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



O membro **dwActivityID**, **dwActivitySize** ou **dwActivityOffset** no [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) foi atualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_ACTIVITYLIST"></span><span id="lineagentstatus_activitylist"></span>**LINEAGENTSTATUS \_ activitylist**
</dt> <dd> <dl> <dt>



O [**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist) foi atualizado. O aplicativo pode chamar [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) para obter a lista atualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_CAPSCHANGE"></span><span id="lineagentstatus_capschange"></span>**LINEAGENTSTATUS \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Os recursos do [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) foram atualizados. O aplicativo pode chamar [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) para obter a lista atualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUP"></span><span id="lineagentstatus_group"></span>**grupo de LINEAGENTSTATUS \_**
</dt> <dd> <dl> <dt>



O [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) foi atualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUPLIST"></span><span id="lineagentstatus_grouplist"></span>**LINEAGENTSTATUS \_ grouplist**
</dt> <dd> <dl> <dt>



O [**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist) foi atualizado. O aplicativo pode chamar [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) para obter a lista atualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_NEXTSTATE"></span><span id="lineagentstatus_nextstate"></span>**LINEAGENTSTATUS \_ nextstate**
</dt> <dd> <dl> <dt>



O membro **dwNextState** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) foi atualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_STATE"></span><span id="lineagentstatus_state"></span>**\_estado LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



O membro **dwState** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) foi atualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDNEXTSTATES"></span><span id="lineagentstatus_validnextstates"></span>**LINEAGENTSTATUS \_ VALIDNEXTSTATES**
</dt> <dd> <dl> <dt>



O membro **dwValidNextStates** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) foi atualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDSTATES"></span><span id="lineagentstatus_validstates"></span>**LINEAGENTSTATUS \_ VALIDSTATES**
</dt> <dd> <dl> <dt>



O membro **dwValidStates** em [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) foi atualizado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 2,0 ou posterior<br/>                                             |
| parâmetro<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist)
</dt> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist)
</dt> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)
</dt> <dt>

[**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)
</dt> <dt>

[**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)
</dt> </dl>

 

 




