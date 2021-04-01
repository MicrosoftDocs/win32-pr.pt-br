---
title: Elemento DisallowStartIfOnBatteries (settingstype)
description: Especifica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Agendador de Tarefas do elemento DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645218"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Elemento DisallowStartIfOnBatteries (settingstype)

Especifica que a tarefa não será iniciada se o computador estiver sendo executado em baterias.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

O elemento **DisallowStartIfOnBatteries** é definido pelo tipo complexo [**settingstype**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                           | Derivado de                                                         | Descrição                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Configurações**](taskschedulerschema-settings-tasktype-element.md) | [**settingstype**](taskschedulerschema-settingstype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

A configuração padrão para esse elemento é true.

Para o desenvolvimento de scripts, essas informações são acessadas por meio da propriedade [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .

Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**ITaskSettings::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que não permite que a tarefa seja executada se o computador estiver sendo executado em baterias.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
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

 

 





