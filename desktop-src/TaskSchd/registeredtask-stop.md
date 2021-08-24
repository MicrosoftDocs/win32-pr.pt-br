---
title: Método RegisteredTask.Stop
description: Para scripts, interrompe a tarefa registrada imediatamente.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Parar o método Agendador de Tarefas
- Método Stop Agendador de Tarefas , objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas , método Stop
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
ms.openlocfilehash: 0496a3b9c8adad0ad4095b6c8aed3888940fd699750350117f4bf503c442f4c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681656"
---
# <a name="registeredtaskstop-method"></a>Método RegisteredTask.Stop

Para scripts, interrompe a tarefa registrada imediatamente.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Reservado. Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A **função RegisteredTask.Stop** interrompe todas as instâncias da tarefa.

Os usuários da conta do sistema podem interromper uma tarefa, os usuários com privilégios de grupo administrador podem interromper uma tarefa e, se um usuário tiver direitos para executar e ler uma tarefa, o usuário poderá interromper a tarefa. Um usuário pode interromper as instâncias de tarefa que estão sendo executados com as mesmas credenciais que a conta de usuário. Em todos os outros casos, o usuário tem acesso negado para interromper a tarefa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





