---
title: Elemento DeleteExpiredTaskAfter (settingstype)
description: Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Agendador de Tarefas do elemento DeleteExpiredTaskAfter
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761809"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a>Elemento DeleteExpiredTaskAfter (settingstype)

Especifica a quantidade de tempo que o Agendador de Tarefas aguardará antes de excluir a tarefa depois que ela expirar. Se nenhum valor for especificado para esse elemento, o serviço de Agendador de Tarefas não excluirá a tarefa. O formato dessa cadeia de caracteres é PnYnMnDTnHnMnS, onde nY é o número de anos, o nM é o número de meses, nD é o número de dias, ' T' é o separador de data/hora, nH é o número de horas, nM é o número de minutos e nS é o número de segundos (por exemplo, PT5M especifica 5 minutos e P1M4DT2H5M especifica um mês, quatro dias, duas horas e cinco minutos). Para obter mais informações sobre o tipo de duração, consulte <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

O elemento **DeleteExpiredTaskAfter** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade DeleteExpiredTaskAfter de ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).

Para desenvolvimento de script, consulte [**TaskSettings. DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de configurações que exclui uma tarefa expirada após uma semana.


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





