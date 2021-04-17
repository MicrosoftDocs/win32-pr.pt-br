---
title: Elemento principal (PrincipalType)
description: Especifica as credenciais de segurança para uma entidade.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Elemento principal Agendador de Tarefas
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782885"
---
# <a name="principal-principaltype-element"></a>Elemento principal (PrincipalType)

Especifica as credenciais de segurança para uma entidade. Essas credenciais definem o contexto de segurança em que uma tarefa é executada.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

O elemento **principal** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                               | Derivado de                                                             | Descrição                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Entidades**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | Especifica as entidades de segurança associadas à tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                      | Type                                                          | Descrição                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **cadeia de caracteres**                                                    | Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas.<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)         | **cadeia de caracteres**                                                    | Especifica o identificador do grupo de usuários necessário para executar tarefas associadas à entidade de segurança.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Especifica o método de logon de segurança necessário para executar as tarefas associadas ao principal.<br/>  |
| [**ID**](taskschedulerschema-userid-principaltype-element.md)           | **cadeia de caracteres**                                                    | Especifica o identificador de usuário necessário para executar tarefas associadas à entidade de segurança.<br/>              |



## <a name="attributes"></a>Atributos



| Nome | Tipo | Descrição                                        |
|------|------|----------------------------------------------------|
| ID   | ID   | Identificador da definição de entidade de segurança.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, as credenciais de segurança para uma entidade são especificadas usando o objeto [**principal**](principal.md) .

Para desenvolvimento em C++, as credenciais de segurança para uma entidade são especificadas usando a interface [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .

Os elementos filho listados acima são definidos pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) . Para obter informações de sequenciamento para esses elementos filho, consulte [**PrincipalType**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Exemplos

O XML a seguir define uma entidade de segurança com um identificador de usuário.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



O XML a seguir define uma entidade de segurança com um identificador de grupo.


```XML
<Principals>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





