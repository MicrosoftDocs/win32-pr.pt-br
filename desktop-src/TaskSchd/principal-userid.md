---
title: Propriedade principal. UserId
description: Para scripts, Obtém ou define o identificador de usuário que é necessário para executar as tarefas associadas à entidade de segurança.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- Agendador de Tarefas da propriedade UserId
- Propriedade UserId Agendador de Tarefas, objeto principal
- Objeto principal Agendador de Tarefas, Propriedade UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085781"
---
# <a name="principaluserid-property"></a>Propriedade principal. UserId

Para scripts, Obtém ou define o identificador de usuário que é necessário para executar as tarefas associadas à entidade de segurança.

## <a name="syntax"></a>Syntax


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Valor da propriedade

O identificador de usuário que é necessário para executar a tarefa.

## <a name="remarks"></a>Comentários

Não defina essa propriedade se um identificador de grupo for especificado na propriedade [**GroupId**](principal-groupid.md) .

Ao ler ou gravar XML para uma tarefa, o identificador de usuário para a entidade de segurança é especificado usando o elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) do esquema de Agendador de tarefas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**Beneficiário**](principal.md)
</dt> <dt>

[**Entidade. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





