---
title: Elemento Version (registrationInfoType)
description: Especifica o número de versão da tarefa.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento de versão Agendador de Tarefas
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63d69b501b12890939f3bd0b146c959278eeaa0d5eb596851a488cef87f0770a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610421"
---
# <a name="version-registrationinfotype-element"></a>Elemento Version (registrationInfoType)

Especifica o número de versão da tarefa.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

O elemento **version** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, a versão de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Version**](registrationinfo-version.md) .

Para o desenvolvimento em C++, a versão de uma tarefa é especificada usando a propriedade [**IRegistrationInfo:: Version**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version) .

## <a name="examples"></a>Exemplos

O XML a seguir define a versão de uma tarefa.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





