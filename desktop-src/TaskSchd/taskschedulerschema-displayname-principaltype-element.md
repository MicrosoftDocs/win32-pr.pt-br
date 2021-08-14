---
title: Elemento DisplayName (PrincipalType)
description: Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Elemento DisplayName Agendador de Tarefas
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ff653a2b2991622b2446bcc0fc74d7063319c2bb6b45556313034a3afb42480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356909"
---
# <a name="displayname-principaltype-element"></a>Elemento DisplayName (PrincipalType)

Especifica o nome da entidade de segurança que é exibida na interface do usuário do Agendador de Tarefas.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

O elemento **DisplayName** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                           | Descrição                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade.<br/> |



## <a name="remarks"></a>Comentários

Para o desenvolvimento de scripts, o nome de exibição da entidade de segurança é especificado usando a propriedade [**principal. DisplayName**](principal-displayname.md) .

Para desenvolvimento em C++, o nome de exibição da entidade de segurança é especificado usando a propriedade [**IPrincipal::D isplayname**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .

## <a name="examples"></a>Exemplos

O XML a seguir define um usando um identificador de grupo e um nome de exibição.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



O XML a seguir define uma entidade de segurança usando um identificador de usuário e um nome de exibição.


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





