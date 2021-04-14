---
title: Tipo complexo de PrincipalType
description: Define o atributo, os elementos filho e as informações de sequenciamento para o elemento principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- tipo complexo de PrincipalType Agendador de Tarefas
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 037013a4b40984df41e52aa13be69c1247b1c05c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455630"
---
# <a name="principaltype-complex-type"></a>Tipo complexo de PrincipalType

Define o atributo, os elementos filho e as informações de sequenciamento para o elemento [**principal**](taskschedulerschema-principal-principaltype-element.md) .

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
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md)                        | string                                                                                   | Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas (UI).<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)                                | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)                  | Especifica o identificador do grupo de usuários que é necessário para executar tarefas associadas à entidade de segurança.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Especifica o método de logon de segurança que é necessário para executar tarefas associadas à entidade.<br/>        |
| [**ProcessTokenSidType**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**processTokenSidType**](taskschedulerschema-processtokensidtype-simpletype.md)        | Especifica os tipos de SID (identificador de segurança do processo) que podem ser usados pelas tarefas.<br/>                              |
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Especifica os privilégios necessários para executar a tarefa.<br/>                                                               |
| [**RunLevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md)                      | Especifica o nível de permissão em que a tarefa será executada.<br/>                                                     |
| [**ID**](taskschedulerschema-userid-principaltype-element.md)                                  | [**não vazio**](taskschedulerschema-nonemptystring-simpletype.md)                  | Especifica o identificador de usuário que é necessário para executar tarefas associadas à entidade de segurança.<br/>              |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                                           |
|------|------|-------------------------------------------------------|
| id   | ID   | Especifica o identificador da entidade de segurança.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





