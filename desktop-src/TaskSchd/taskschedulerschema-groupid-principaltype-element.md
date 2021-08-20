---
title: Elemento GroupId (principalType)
description: Especifica o identificador do grupo de usuários necessário para executar as tarefas associadas à entidade de entidade.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Elemento GroupId Agendador de Tarefas
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131835"
---
# <a name="groupid-principaltype-element"></a>Elemento GroupId (principalType)

Especifica o identificador do grupo de usuários necessário para executar as tarefas associadas à entidade de entidade.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

O **elemento GroupId** é definido pelo tipo [**complexo principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                           | Descrição                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal**](taskschedulerschema-principal-principaltype-element.md) | [**Principaltype**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade de segurança.<br/> |



## <a name="remarks"></a>Comentários

Não é possível especificar um identificador de grupo e um identificador de usuário ao mesmo tempo. Especifique os [**elementos UserId**](taskschedulerschema-userid-principaltype-element.md) ou **GroupId,** mas não ambos.

Para desenvolvimento de scripts, o identificador de grupo da entidade de entidade é especificado usando a [**propriedade Principal.GroupId.**](principal-groupid.md)

Para desenvolvimento em C++, o identificador de grupo da entidade de serviço é especificado usando a [**propriedade IPrincipal::GroupId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid)

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que usa esse elemento, consulte [Xml (Exemplo de Gatilho de Logon).](logon-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





