---
title: Método RegisteredTask. Stop
description: Para scripts, o interrompe a tarefa registrada imediatamente.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Agendador de Tarefas do método Stop
- Método Stop Agendador de Tarefas, objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, método Stop
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369880"
---
# <a name="registeredtaskstop-method"></a>Método RegisteredTask. Stop

Para scripts, o interrompe a tarefa registrada imediatamente.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Reservado. Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A função **RegisteredTask. Stop** interrompe todas as instâncias da tarefa.

Os usuários da conta do sistema podem interromper uma tarefa, os usuários com privilégios de grupo de administradores podem interromper uma tarefa e, se um usuário tiver direitos para executar e ler uma tarefa, o usuário poderá interromper a tarefa. Um usuário pode interromper as instâncias de tarefa que estão sendo executadas com as mesmas credenciais que a conta de usuário. Em todos os outros casos, o acesso ao usuário é negado para interromper a tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





