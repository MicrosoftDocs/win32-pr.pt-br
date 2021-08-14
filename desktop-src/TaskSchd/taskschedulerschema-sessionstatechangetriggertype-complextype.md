---
title: Tipo complexo sessionStateChangeTriggerType
description: Define os elementos usados para criar um gatilho de tarefa para conexão ou desconexão do console, conexão remota ou desconexão, ou notificações de bloqueio ou desbloqueio de estação de trabalho.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- tipo complexo sessionStateChangeTriggerType Agendador de Tarefas
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e9779ae2f609f721e4417dc08698e9720bd4cbe03c2b59787edcf862c8d284d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990936"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Tipo complexo sessionStateChangeTriggerType

Define os elementos usados para criar um gatilho de tarefa para conexão ou desconexão do console, conexão remota ou desconexão, ou notificações de bloqueio ou desbloqueio de estação de trabalho.

``` syntax
<xs:complexType name="sessionStateChangeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:element name="StateChange"
                    type="sessionStateChangeType"
                    minOccurs="1"
                    maxOccurs="1"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                      | Type                                                                                    | Descrição                                                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Atrasar**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Especifica um valor que indica o comprimento do atraso antes que uma tarefa seja iniciada quando uma alteração de estado de sessão do Servidor de Terminal é detectada.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Especifica o tipo de alteração de sessão do Servidor de Terminal que dispararia uma iniciação de tarefa.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                 | Especifica o usuário para a sessão do Servidor de Terminal. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.<br/>              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 





