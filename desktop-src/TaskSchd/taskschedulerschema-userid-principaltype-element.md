---
title: Elemento UserId (PrincipalType)
description: Especifica o identificador de usuário necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- Elemento UserId Agendador de Tarefas
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 955dcc93b826b4f86bffd3371ab9907e56dfe7f35649aee603cb18716868f535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959526"
---
# <a name="userid-principaltype-element"></a>Elemento UserId (PrincipalType)

Especifica o identificador de usuário necessário para executar as tarefas associadas à entidade de segurança.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

O elemento **userid** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                           | Descrição                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade.<br/> |



## <a name="remarks"></a>Comentários

O elemento **userid** e o elemento [**Logontype**](taskschedulerschema-logontype-principaltype-element.md) são usados juntos para definir o usuário necessário para executar as tarefas que usam essa entidade de segurança.

Você não pode especificar um identificador de usuário e um identificador de grupo ao mesmo tempo. Especifique o elemento **userid** ou [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) , mas não ambos.

Para o desenvolvimento de scripts, o identificador de usuário é especificado usando a propriedade [**principal. UserID**](principal-userid.md) .

Para desenvolvimento em C++, o identificador de usuário é especificado usando a propriedade [**IPrincipal:: userid**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

## <a name="examples"></a>Exemplos

O XML a seguir define um princípio usando um identificador de usuário.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
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

 

 





