---
title: Elemento AllowStartOnDemand (settingsType)
description: Especifica que a tarefa pode ser iniciada usando o comando Executar ou o menu Contexto.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Elemento AllowStartOnDemand Agendador de Tarefas
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: be89197c4ae88188fc1d2a746c40d69e385edc7ba08aaf2d3bf29067ee5f4a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119516986"
---
# <a name="allowstartondemand-settingstype-element"></a>Elemento AllowStartOnDemand (settingsType)

Especifica que a tarefa pode ser iniciada usando o comando Executar ou o menu Contexto.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

O **elemento AllowStartOnDemand** é definido pelo tipo complexo [**settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Quando esse elemento é definido como True, a tarefa pode ser iniciada independentemente de quando qualquer gatilho inicia a tarefa.

Para desenvolvimento em C++, consulte a [**propriedade AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Para desenvolvimento de scripts, [**consulte TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que permite o início da demanda, consulte [Exemplo de gatilho de tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





