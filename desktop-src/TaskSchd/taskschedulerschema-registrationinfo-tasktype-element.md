---
title: Elemento RegistrationInfo (taskType)
description: Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.
ms.assetid: f3961bad-e9a3-4626-87ed-9639d912717d
keywords:
- informações de registro Agendador de Tarefas, elemento XML
- Agendador de Tarefas do elemento RegistrationInfo
topic_type:
- apiref
api_name:
- RegistrationInfo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bcae83c4ecc87f259087ea84f8ca4b63bd83e574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455502"
---
# <a name="registrationinfo-tasktype-element"></a>Elemento RegistrationInfo (taskType)

Especifica informações administrativas sobre a tarefa, como o autor da tarefa e a data em que a tarefa é registrada.

``` syntax
<xs:element name="RegistrationInfo"
    type="registrationInfoType"
    minOccurs="0"
 />
```

O elemento **RegistrationInfo** é definido pelo tipo complexo [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                          | Derivado de                                                 | Descrição                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Tarefa**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Define a tarefa que é executada pelo serviço de Agendador de Tarefas.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                                  | Type     | Descrição                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autor (registrationInfoType)**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Especifica o autor da tarefa.<br/>                                                                              |
| [**Data (registrationInfoType)**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Especifica a data e a hora em que a tarefa é registrada.<br/>                                                       |
| [**Descrição (registrationInfoType)**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Especifica a descrição da tarefa.<br/>                                                                         |
| [**Documentação (registrationInfoType)**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Especifica qualquer documentação adicional para a tarefa.<br/>                                                           |
| [**SecurityDescriptor (registrationInfoType)**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Especifica o descritor de segurança da tarefa.<br/>                                                                 |
| [**Origem (registrationInfoType)**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Especifica de onde a tarefa foi originada. Por exemplo, de um componente, um serviço, um aplicativo ou um usuário.<br/> |
| [**URI (registrationInfoType)**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Especifica o URI da tarefa.<br/>                                                                                 |
| [**Versão (registrationInfoType)**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Especifica o número de versão da tarefa.<br/>                                                                      |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, as informações de registro de uma tarefa são especificadas usando a propriedade [**TaskDefinition. RegistrationInfo**](taskdefinition-registrationinfo.md) .

Para desenvolvimento em C++, as informações de registro de uma tarefa são especificadas usando a [**Propriedade RegistrationInfo de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_registrationinfo).

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

 

 





