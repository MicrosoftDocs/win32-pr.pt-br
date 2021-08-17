---
title: Método RegisteredTask. getruntimes
description: Para scripts, obtém as horas em que a tarefa registrada está agendada para ser executada durante um período especificado.
ms.assetid: fc3d93eb-3186-419f-9f6f-7d54f8ade1ad
keywords:
- Método getruntimes Agendador de Tarefas
- Método getruntimes Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método getruntimes
topic_type:
- apiref
api_name:
- RegisteredTask.GetRunTimes
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303dd08c576f31946207241b086fe945b3f1ac275c596496139d19f507670e30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759661"
---
# <a name="registeredtaskgetruntimes-method"></a>Método RegisteredTask. getruntimes

Para scripts, obtém as horas em que a tarefa registrada está agendada para ser executada durante um período especificado.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.GetRunTimes( _
  ByVal begin, _
  ByVal end, _
  ByRef count, _
  ByRef rgstTaskTimes _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iniciar* \[ no\]
</dt> <dd>

A hora de início da consulta.

</dd> <dt>

*fim* \[ no\]
</dt> <dd>

A hora de término da consulta.

</dd> <dt>

*contagem* \[ de fora\]
</dt> <dd>

O número de horas agendadas em que a tarefa será executada.

</dd> <dt>

*rgstTaskTimes* \[ fora\]
</dt> <dd>

Os horários agendados em que a tarefa será executada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se a tarefa registrada contiver gatilhos que são desabilitados individualmente, esses gatilhos ainda afetarão o próximo tempo de execução agendado que é retornado, embora estejam desabilitados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





