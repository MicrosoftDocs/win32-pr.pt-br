---
title: Elemento RunLevel (runLevelType)
description: Contém um valor que especifica o nível de contexto de segurança para executar a tarefa.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Agendador de Tarefas do elemento RunLevel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295909"
---
# <a name="runlevel-runleveltype-element"></a>Elemento RunLevel (runLevelType)

Contém um valor que especifica o nível de contexto de segurança para executar a tarefa. Você pode especificar para executar uma tarefa usando privilégios mínimos ou privilégios elevados. Um valor de 0 especifica a execução da tarefa com privilégios mais baixos e um valor de 1 especifica para executar a tarefa com privilégios elevados.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

O elemento **runlevel** é definido pelo tipo simples [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                                  | Derivado de                                                           | Descrição                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Entidade de segurança (PrincipalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade. Essas credenciais definem o contexto de segurança em que uma tarefa é executada. <br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade runlevel de IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Para desenvolvimento de script, consulte [**principal. runlevel**](principal-runlevel.md).

Se uma tarefa for registrada usando a conta de **\\ Administrador interno** ou as contas [LocalSystem](/windows/desktop/Services/localsystem-account) ou [LocalService](/windows/desktop/Services/localservice-account) , a propriedade [**runlevel**](principal-runlevel.md) será ignorada. O valor do atributo também será ignorado se o UAC ( [controle de conta de usuário](/windows/desktop/SecAuthZ/user-account-control) ) estiver desativado.

Se uma tarefa for registrada usando o grupo **Administradores** para o contexto de segurança da tarefa, você também deverá definir a propriedade [**runlevel**](principal-runlevel.md) como "highestAvailable" para executar a tarefa. Para obter mais informações, consulte [contextos de segurança para tarefas](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

