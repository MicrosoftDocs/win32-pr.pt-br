---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Especifica que o Agendador de Tarefas interromperá a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Agendador de Tarefas do elemento StopOnIdleEnd
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e6497ca88d43b96096ee6a23ee81a322b0f397757466ed8cf09dd1b3cd45fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356054"
---
# <a name="stoponidleend-idlesettingstype-element"></a>Elemento StopOnIdleEnd (idleSettingsType)

Especifica que o Agendador de Tarefas interromperá a tarefa se a condição de ociosidade terminar antes de a tarefa ser concluída.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

O elemento **StopOnIdleEnd** é definido pelo tipo complexo [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                       | Derivado de                                                                 | Descrição                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Especifica como a Agendador de Tarefas executa tarefas quando o computador está em um estado ocioso.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade StopOnIdleEnd de IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).

Para desenvolvimento de script, consulte [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).

## <a name="examples"></a>Exemplos

O XML a seguir define uma configuração ociosa que indica que a tarefa não deve ser executada quando a condição ociosa terminar.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
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

 

 





