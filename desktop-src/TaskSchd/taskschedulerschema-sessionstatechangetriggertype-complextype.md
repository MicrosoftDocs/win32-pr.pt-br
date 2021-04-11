---
title: Tipo complexo sessionStateChangeTriggerType
description: Define os elementos usados para criar um gatilho de tarefa para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.
ms.assetid: 0d452476-1e1f-417d-a97a-5f39d80145f2
keywords:
- Agendador de Tarefas tipo complexo sessionStateChangeTriggerType
topic_type:
- apiref
api_name:
- sessionStateChangeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8eb3ad02aef3f5bbbc078f8eafa52f3439819cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295908"
---
# <a name="sessionstatechangetriggertype-complex-type"></a>Tipo complexo sessionStateChangeTriggerType

Define os elementos usados para criar um gatilho de tarefa para conexão ou desconexão do console, conexão remota ou desconexão ou bloqueio de estação de trabalho ou notificações de desbloqueio.

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
| [**Retardo**](taskschedulerschema-delay-sessionstatechangetriggertype-element.md)             | duration                                                                                | Especifica um valor que indica o comprimento do atraso antes que uma tarefa seja iniciada quando uma alteração de estado de sessão de Terminal Server for detectada.<br/> |
| [**StateChange**](taskschedulerschema-statechange-sessionstatechangetriggertype-element.md) | [**sessionStateChangeType**](taskschedulerschema-sessionstatechangetype-simpletype.md) | Especifica o tipo de Terminal Server alteração de sessão que dispararia uma inicialização de tarefa.<br/>                                                     |
| [**ID**](taskschedulerschema-userid-sessionstatechangetriggertype-element.md)           | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)                 | Especifica o usuário para a sessão de Terminal Server. Quando uma alteração de estado de sessão é detectada para esse usuário, uma tarefa é iniciada.<br/>              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





