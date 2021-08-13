---
title: Tipo complexo registrationInfoType
description: Define os elementos filho e as informações de sequenciamento para o elemento RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Agendador de Tarefas tipo complexo registrationInfoType
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 704fcb3205f032654ef6a666dd119dec34f88992018f16b1715ba4982847149d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131656"
---
# <a name="registrationinfotype-complex-type"></a>Tipo complexo registrationInfoType

Define os elementos filho e as informações de sequenciamento para o elemento [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                           | Type     | Descrição                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Autor**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Especifica o autor da tarefa.<br/>                                                                       |
| [**Date**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Especifica a data e a hora em que a tarefa é registrada.<br/>                                                |
| [**Descrição**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Especifica a descrição da tarefa.<br/>                                                                  |
| [**Documentação**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Especifica qualquer documentação adicional para a tarefa.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Especifica o descritor de segurança da tarefa.<br/>                                                          |
| [**Original**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Especifica de onde a tarefa foi originada. Por exemplo, de um componente, serviço, aplicativo ou usuário.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Especifica o URI da tarefa.<br/>                                                                          |
| [**Versão**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Especifica o número de versão da tarefa.<br/>                                                               |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





