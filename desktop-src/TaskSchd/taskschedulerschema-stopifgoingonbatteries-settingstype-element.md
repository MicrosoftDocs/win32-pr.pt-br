---
title: Elemento StopIfGoingOnBatteries (settingstype)
description: Especifica que a tarefa será interrompida se o computador estiver indo para baterias.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Agendador de Tarefas do elemento StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50b92be11400d1dbb223115f11334e2a596e94e9df1fd018ce16e4a646c84825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516094"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>Elemento StopIfGoingOnBatteries (settingstype)

Especifica que a tarefa será interrompida se o computador estiver indo para baterias.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

O elemento **StopIfGoingOnBatteries** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

A configuração padrão para esse elemento é false. Observe que o valor padrão foi alterado de versões anteriores do Agendador de Tarefas.

Para o desenvolvimento de scripts, essa configuração é especificada usando a propriedade [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) .

Para desenvolvimento em C++, essa configuração é especificada usando a propriedade [**ITaskSettings:: StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de configurações que permite um encerramento rígido da tarefa.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





