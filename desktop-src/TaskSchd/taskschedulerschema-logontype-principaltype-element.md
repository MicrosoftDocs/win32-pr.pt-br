---
title: Elemento Logontype (dirigetype)
description: Especifica o método de logon de segurança necessário para executar as tarefas associadas ao principal.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Agendador de Tarefas do elemento Logontype
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9121179b744857d5e7d0bec5a2ae814c603c6b1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885848"
---
# <a name="logontype-principaltype-element"></a>Elemento Logontype (dirigetype)

Especifica o método de logon de segurança necessário para executar as tarefas associadas ao principal.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

O elemento **Logontype** é definido pelo tipo complexo de [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                           | Description                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Beneficiário**](taskschedulerschema-principal-principaltype-element.md) | [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) | Especifica as credenciais de segurança para uma entidade.<br/> |



## <a name="remarks"></a>Comentários

O elemento **Logontype** e o elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) são usados juntos para definir o usuário necessário para executar as tarefas que usam essa entidade de segurança.

Para o desenvolvimento de scripts, o tipo de logon para a entidade de segurança é especificado pela propriedade [**principal. Logontype**](principal-logontype.md) .

Para desenvolvimento em C++, o tipo de logon para a entidade de segurança é especificado pela propriedade [**IPrincipal:: Logontype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .

Esse elemento (definido pelo tipo simples de [**Logontype**](taskschedulerschema-logontype-simpletype.md) ) deve ter um dos valores a seguir.

-   S4U: o usuário deve fazer logon usando um serviço de logon de usuário (S4U). Quando um logon S4U é usado, nenhuma senha é armazenada pelo sistema e não há acesso à rede ou aos arquivos criptografados.
-   Senha: o usuário deve fazer logon usando uma senha.
-   InteractiveToken: o usuário já deve estar conectado. A tarefa será executada somente em uma sessão interativa existente.

Para uma tarefa que contém uma ação de caixa de mensagem, a caixa de mensagem será exibida se a tarefa for ativada e a tarefa tiver um tipo de logon interativo. Para definir o tipo de logon da tarefa como interativo, especifique **InteractiveToken** no elemento **&lt; Logontype &gt;** da entidade de segurança da tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





