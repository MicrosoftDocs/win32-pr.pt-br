---
title: Elemento GroupId (dirigetype)
description: Especifica o identificador do grupo de usuários necessário para executar as tarefas associadas à entidade de segurança.
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
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009631"
---
# <a name="groupid-principaltype-element"></a>Elemento GroupId (dirigetype)

Especifica o identificador do grupo de usuários necessário para executar as tarefas associadas à entidade de segurança.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

O elemento **GroupId** é definido pelo tipo complexo [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                           | Descrição                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Beneficiário**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade.<br/> |



## <a name="remarks"></a>Comentários

Você não pode especificar um identificador de grupo e um identificador de usuário ao mesmo tempo. Especifique os elementos [**userid**](taskschedulerschema-userid-principaltype-element.md) ou **GroupId** , mas não ambos.

Para o desenvolvimento de script, o identificador de grupo da entidade de segurança é especificado usando a propriedade [**principal. GroupId**](principal-groupid.md) .

Para desenvolvimento em C++, o identificador de grupo da entidade de segurança é especificado usando a propriedade [**IPrincipal:: GroupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa esse elemento, consulte [exemplo de gatilho de logon (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





