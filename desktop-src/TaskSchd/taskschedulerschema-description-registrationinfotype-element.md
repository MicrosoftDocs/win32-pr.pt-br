---
title: Elemento Description (registrationInfoType)
description: Especifica a descrição da tarefa.
ms.assetid: bf3552eb-01a6-4651-ae43-4b4e8eef3faf
keywords:
- Elemento de descrição Agendador de Tarefas
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 80815a1502060af231cae1b93b964b80345891e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644480"
---
# <a name="description-registrationinfotype-element"></a>Elemento Description (registrationInfoType)

Especifica a descrição da tarefa.

``` syntax
<xs:element name="Description"
    type="string"
    minOccurs="0"
 />
```

O elemento **Description** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, a descrição de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Description**](registrationinfo-description.md) .

Para desenvolvimento em C++, a descrição de uma tarefa é especificada usando a propriedade [**IRegistrationInfo::D Descrição**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_description) .

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

 

 





