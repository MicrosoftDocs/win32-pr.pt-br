---
title: Elemento RestartOnIdle (idleSettingsType)
description: Especifica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.
ms.assetid: 7a7a388c-8dc9-4106-82c1-3435d9f89866
keywords:
- Elemento RestartOnIdle Agendador de Tarefas
topic_type:
- apiref
api_name:
- RestartOnIdle
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16a636ebc052bb04a150390659909f0b73cae78871acaacfb4ba529ea2d8e917
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575136"
---
# <a name="restartonidle-idlesettingstype-element"></a>Elemento RestartOnIdle (idleSettingsType)

Especifica se a tarefa é reiniciada quando o computador entra em uma condição ociosa mais de uma vez.

``` syntax
<xs:element name="RestartOnIdle"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O **elemento RestartOnIdle** é definido pelo tipo complexo [**idleSettingsType.**](taskschedulerschema-idlesettingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica como o Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/> |



## <a name="remarks"></a>Comentários

Esse elemento será usado somente se [**o elemento TerminateOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) estiver definido como True.

Para desenvolvimento de script, essas configurações de tarefa são especificadas usando a [**propriedade IdleSettings.RestartOnIdle.**](idlesettings-restartonidle.md)

Para desenvolvimento em C++, essas configurações de tarefa são especificadas usando a [**propriedade IIdleSettings::RestartOnIdle.**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle)

## <a name="examples"></a>Exemplos

O XML a seguir define uma configuração ociosa que indica que a tarefa não deve ser reiniciada quando a condição ociosa é reiniciada.


```XML
<IdleSettings>
     <TerminateOnIdleEnd>true</TerminateOnIdleEnd>
     <RestartOnIdle>true</RestartOnIdle>
</IdleSettings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





