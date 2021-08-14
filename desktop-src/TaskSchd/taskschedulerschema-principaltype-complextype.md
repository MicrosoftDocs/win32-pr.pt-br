---
title: Tipo complexo principalType
description: Define o atributo, elementos filho e informações de sequenciamento para o elemento Principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- tipo complexo principalType Agendador de Tarefas
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6b2d7e71642ab0294f6e930eef40c5841aa5832fcc3a8d1c45aef2d7e80bbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611908"
---
# <a name="principaltype-complex-type"></a>Tipo complexo principalType

Define o atributo, elementos filho e informações de sequenciamento para o [**elemento Principal.**](taskschedulerschema-principal-principaltype-element.md)

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                             | Type                                                                                     | Descrição                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**Displayname**](taskschedulerschema-displayname-principaltype-element.md)                        | string                                                                                   | Especifica o nome da entidade de entidade que é exibida na interface do usuário Agendador de Tarefas usuário.<br/>                 |
| [**Groupid**](taskschedulerschema-groupid-principaltype-element.md)                                | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Especifica o identificador do grupo de usuários necessário para executar tarefas associadas à entidade de entidade.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Especifica o método de logon de segurança necessário para executar tarefas associadas à entidade de segurança.<br/>        |
| [**ProcessTokenSidType**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processTokenSidType**](taskschedulerschema-processtokensidtype-simpletype.md)        | Especifica os tipos de SID (identificador de segurança) do processo que podem ser usados por tarefas.<br/>                              |
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Especifica os privilégios necessários para executar a tarefa.<br/>                                                               |
| [**Runlevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md)                      | Especifica o nível de permissão em que a tarefa será executado.<br/>                                                     |
| [**Userid**](taskschedulerschema-userid-principaltype-element.md)                                  | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)                  | Especifica o identificador de usuário necessário para executar tarefas associadas à entidade de entidade.<br/>              |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                                           |
|------|------|-------------------------------------------------------|
| id   | ID   | Especifica o identificador da entidade de entidade de trabalho.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas complexos de esquema](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





