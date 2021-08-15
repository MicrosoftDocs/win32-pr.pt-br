---
title: Elemento RunOnlyIfNetworkAvailable (settingsType)
description: Especifica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.
ms.assetid: b7b804d3-b31a-4d70-9ba5-805a285e278e
keywords:
- Elemento RunOnlyIfNetworkAvailable Agendador de Tarefas
topic_type:
- apiref
api_name:
- RunOnlyIfNetworkAvailable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a3680ba3c29dc0d258a48aa16ae7923e3761eda30f198384fecfbf238e2933cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991026"
---
# <a name="runonlyifnetworkavailable-settingstype-element"></a>Elemento RunOnlyIfNetworkAvailable (settingsType)

Especifica que o Agendador de Tarefas executará a tarefa somente quando uma rede estiver disponível.

``` syntax
<xs:element name="RunOnlyIfNetworkAvailable"
    type="boolean"
    default="false"
    minOccurs="0"
 />
```

O **elemento RunOnlyIfNetworkAvailable** é definido pelo [**tipo complexo settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte [**Propriedade RunOnlyIfNetworkAvailable de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_runonlyifnetworkavailable).

Para desenvolvimento de scripts, [**consulte TaskSettings.RunOnlyIfNetworkAvailable.**](tasksettings-runonlyifnetworkavailable.md)

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de configurações que permite que a tarefa inicie somente se uma rede estiver disponível.


```XML
<Settings>
    <RunOnlyIfNetworkAvailable>true</RunOnlyIfNetworkAvailable>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





