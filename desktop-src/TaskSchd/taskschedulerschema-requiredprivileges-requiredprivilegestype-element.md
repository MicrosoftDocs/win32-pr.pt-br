---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Especifica os privilégios exigidos pela tarefa.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Agendador de Tarefas do elemento RequiredPrivileges
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e395a61aace07dccb27eab04d9c0299115c25f16d84cd42e3d607435478f8060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611483"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Elemento RequiredPrivileges (requiredPrivilegesType)

Especifica os privilégios exigidos pela tarefa.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

O elemento **RequiredPrivileges** é definido pelo tipo complexo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                           | Descrição                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Entidade de segurança (PrincipalType)**](taskschedulerschema-principal-principaltype-element.md) | [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Exemplos

O XML a seguir define o uso de um identificador de grupo e os privilégios necessários.


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





