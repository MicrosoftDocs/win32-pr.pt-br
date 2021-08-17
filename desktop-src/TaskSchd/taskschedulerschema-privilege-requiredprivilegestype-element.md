---
title: Elemento Privilege (requiredPrivilegesType)
description: Especifica o direito de uma tarefa executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Elemento Privilege Agendador de Tarefas
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f181c2dbe21e31c752a44a4a3b0e27abd0f9396939c9a9dcee3127f796760527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758314"
---
# <a name="privilege-requiredprivilegestype-element"></a>Elemento Privilege (requiredPrivilegesType)

Especifica o direito de uma tarefa executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

O **elemento Privilege** é definido pelo tipo complexo [**requiredPrivilegesType.**](taskschedulerschema-requiredprivilegestype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                             | Derivado de                                                                             | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, essas informações são acessadas por meio da [**propriedade IPrincipal2::RequiredPrivilege.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege)

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento de configurações que especifica o direito de uma tarefa executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.


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
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





