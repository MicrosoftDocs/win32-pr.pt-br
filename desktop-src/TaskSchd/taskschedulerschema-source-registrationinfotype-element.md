---
title: Elemento Source (registrationInfoType)
description: Especifica de onde a tarefa foi originada. Por exemplo, de um componente, um serviço, um aplicativo ou um usuário.
ms.assetid: 174e2aac-7cd0-4c19-9441-2c93a3260c6f
keywords:
- Elemento de origem Agendador de Tarefas
topic_type:
- apiref
api_name:
- Source
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65437fa0e06c303c7c2c29151f33f74f1678296d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369334"
---
# <a name="source-registrationinfotype-element"></a>Elemento Source (registrationInfoType)

Especifica de onde a tarefa foi originada. Por exemplo, de um componente, um serviço, um aplicativo ou um usuário.

``` syntax
<xs:element name="Source"
    type="string"
    minOccurs="0"
 />
```

O elemento **Source** é definido pelo tipo complexo [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                           | Derivado de                                                                         | Descrição                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, a origem de uma tarefa é especificada usando a propriedade [**RegistrationInfo. Source**](registrationinfo-source.md) .

Para desenvolvimento em C++, a origem de uma tarefa é especificada usando a propriedade [**IRegistrationInfo:: Source**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_source) .

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

 

 





