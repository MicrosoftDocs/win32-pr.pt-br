---
title: Elemento AllowStartOnDemand (settingstype)
description: Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Agendador de Tarefas do elemento AllowStartOnDemand
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918146"
---
# <a name="allowstartondemand-settingstype-element"></a>Elemento AllowStartOnDemand (settingstype)

Especifica que a tarefa pode ser iniciada usando o comando executar ou o menu de contexto.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

O elemento **AllowStartOnDemand** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Quando esse elemento é definido como true, a tarefa pode ser iniciada independentemente de quando os gatilhos iniciam a tarefa.

Para desenvolvimento em C++, consulte a [**Propriedade AllowDemandStart de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Para desenvolvimento de script, consulte [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que permite iniciar a demanda, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





