---
title: Elemento Privilege (requiredPrivilegesType)
description: Especifica a direita de uma tarefa para executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Agendador de Tarefas de elemento de privilégio
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455703"
---
# <a name="privilege-requiredprivilegestype-element"></a>Elemento Privilege (requiredPrivilegesType)

Especifica a direita de uma tarefa para executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

O elemento **Privilege** é definido pelo tipo complexo [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                             | Derivado de                                                                             | Descrição                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Contém as configurações que o Agendador de Tarefas usa para executar a tarefa.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, essas informações são acessadas por meio da propriedade [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Exemplos

O XML a seguir define um elemento Settings que especifica a direita de uma tarefa para executar várias operações relacionadas ao sistema, como desligar o sistema, carregar drivers de dispositivo ou alterar a hora do sistema.


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





