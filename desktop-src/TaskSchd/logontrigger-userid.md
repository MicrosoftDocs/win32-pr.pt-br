---
title: Propriedade LogonTrigger. UserId
description: Para scripts, Obtém ou define o identificador do usuário.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- Agendador de Tarefas da propriedade UserId
- Propriedade UserId Agendador de Tarefas, objeto LogonTrigger
- Objeto LogonTrigger Agendador de Tarefas, Propriedade UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369340"
---
# <a name="logontriggeruserid-property"></a>Propriedade LogonTrigger. UserId

Para scripts, Obtém ou define o identificador do usuário.

## <a name="syntax"></a>Syntax


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador do usuário. Por exemplo, "mydomain \\ myname" ou para uma conta local, "Administrator".

Essa propriedade pode estar em um dos seguintes formatos:

-   Nome de usuário ou SID: a tarefa é iniciada quando o usuário faz logon no computador.
-   NULL: a tarefa é iniciada quando qualquer usuário faz logon no computador.

## <a name="remarks"></a>Comentários

Se você quiser que uma tarefa seja disparada quando qualquer membro de um grupo fizer logon no computador em vez de quando um usuário específico fizer logon, não atribua um valor à propriedade **LogonTrigger. UserID** . Em vez disso, crie um gatilho de logon com uma propriedade **LogonTrigger. UserID** vazia e atribua um valor para a entidade de segurança da tarefa usando a propriedade [**principal. GroupId**](principal-groupid.md) .

Ao ler ou gravar XML para uma tarefa, o identificador de usuário de logon é especificado usando o elemento [**userid**](taskschedulerschema-userid-logontriggertype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LogonTrigger**](logontrigger.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





