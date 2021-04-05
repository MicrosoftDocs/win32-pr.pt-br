---
title: Elemento Author (registrationInfoType)
description: Especifica o autor da tarefa.
ms.assetid: 1faa4952-0737-4313-afa5-4a9bad5daaff
keywords:
- Elemento de autor Agendador de Tarefas
topic_type:
- apiref
api_name:
- Author
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d368093a266827004cddf23dc7ba5d82f108f99f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918667"
---
# <a name="author-registrationinfotype-element"></a>Elemento Author (registrationInfoType)

Especifica o autor da tarefa.

``` syntax
<xs:element name="Author"
    type="string"
    minOccurs="0"
 />
```

O elemento **Author** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o autor da tarefa é especificado usando a propriedade [**RegistrationInfo. Author**](registrationinfo-author.md) .

Para desenvolvimento em C++, o autor da tarefa é especificado usando a propriedade [**IRegistrationInfo:: Author**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_author) .

## <a name="examples"></a>Exemplos

O XML a seguir define o autor de uma tarefa.


```XML
<RegistrationInfo>
    <Author></Author>
 </RegistrationInfo>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





