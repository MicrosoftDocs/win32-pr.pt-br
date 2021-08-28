---
title: Elemento RestartOnFailure (settingstype)
description: Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.
ms.assetid: c90d8c62-dd97-4ea6-bd87-37b0915e0b38
keywords:
- Agendador de Tarefas do elemento RestartOnFailure
topic_type:
- apiref
api_name:
- RestartOnFailure
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bfe29be7dd329def41e8a6726f141a850eb2daecd05e05d6b5988f543f64864c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072436"
---
# <a name="restartonfailure-settingstype-element"></a>Elemento RestartOnFailure (settingstype)

Especifica que o Agendador de Tarefas tentará reiniciar a tarefa se a tarefa falhar por algum motivo.

``` syntax
<xs:element name="RestartOnFailure"
    type="restartType"
    minOccurs="0"
 />
```

O elemento **RestartOnFailure** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                              | Type         | Descrição                                                                                        |
|----------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------|
| [**Contagem**](taskschedulerschema-count-restarttype-element.md)       | unsignedByte | Especifica o número de vezes que o Agendador de Tarefas tentará reiniciar a tarefa.<br/> |
| [**Intervalo**](taskschedulerschema-interval-restarttype-element.md) | duration     | Especifica por quanto tempo o Agendador de Tarefas tentará reiniciar a tarefa.<br/>                 |



## <a name="remarks"></a>Comentários

Quando um aplicativo especifica as configurações de tarefa, essas informações são acessadas por meio das propriedades [**RestartCount**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartcount) e [**RestartInterval**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_restartinterval) da interface [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) . Para scripts, essas informações são acessadas por meio das propriedades [**TaskSettings. RestartCount**](tasksettings-restartcount.md) e [**TaskSettings. RestartInterval**](tasksettings-restartinterval.md) .

Ambos os elementos filho devem ser definidos para especificar como o Agendador de Tarefas reinicia a tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





