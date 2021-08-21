---
title: Método RegisteredTask.RunEx
description: Para scripts, executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Método RunEx Agendador de Tarefas
- Método RunEx Agendador de Tarefas , objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas , método RunEx
topic_type:
- apiref
api_name:
- RegisteredTask.RunEx
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecea66d57bf473b5000e84c707e652f1c49431a840da5cc50e43f9e091c3eefb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943388"
---
# <a name="registeredtaskrunex-method"></a>Método RegisteredTask.RunEx

Para scripts, executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.RunEx( _
  ByVal params, _
  ByVal flags, _
  ByVal sessionID, _
  ByRef runningTask _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*params* \[ Em\]
</dt> <dd>

Os parâmetros usados como valores nas ações da tarefa. Para não especificar nenhum valor de parâmetro para as ações da tarefa, de definido esse parâmetro como **Nothing**. Caso contrário, um único valor de cadeia de caracteres ou uma matriz de valores de cadeia de caracteres pode ser especificado.

Os valores de cadeia de caracteres especificados são emparelhados com nomes e armazenados como pares nome-valor. Se você especificar um único valor de cadeia de caracteres, Arg0 será o nome atribuído ao valor. O valor pode ser usado na ação de tarefa em que a variável $(Arg0) é usada nas propriedades da ação.

Se você passar valores como "0", "100" e "250" como uma matriz de valores de cadeia de caracteres, "0" substituirá as variáveis $(Arg0), "100" substituirá as variáveis $(Arg1) e "250" substituirá as variáveis $(Arg2) usadas nas propriedades de ação.

Um máximo de 32 valores de cadeia de caracteres pode ser especificado.

Para obter mais informações e uma lista de propriedades de ação que podem usar variáveis $(Arg0), $(Arg1), ..., $(Arg32) em seus valores, consulte [Ações de tarefa](task-actions.md).

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Uma [constante TASK RUN \_ \_ FLAGS](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) que define como a tarefa é executado.

</dd> <dt>

*sessionID* \[ Em\]
</dt> <dd>

A sessão do servidor terminal na qual você deseja iniciar a tarefa.

Se a constante TASK \_ RUN \_ USE SESSION \_ \_ ID (0x4) não for passada para o parâmetro *flags,* o valor especificado nesse parâmetro será ignorado. Se a constante TASK RUN USE SESSION ID for passada para o parâmetro flags e o valor sessionID for menor ou igual \_ \_ a \_ \_ 0,  um erro de argumento inválido será retornado.

Se a constante TASK RUN USE SESSION ID for passada para o parâmetro flags e o valor sessionID for uma ID de sessão válida maior que 0 e se nenhum valor for especificado para o parâmetro de usuário, o serviço Agendador de Tarefas tentará iniciar a tarefa interativamente como o usuário que está conectado à sessão \_ \_ \_ \_ especificada.  

Se a constante TASK RUN USE SESSION ID for passada para o parâmetro flags e o valor sessionID for uma ID de sessão válida maior que 0 e se um usuário for especificado no parâmetro de usuário, o serviço Agendador de Tarefas tentará iniciar a tarefa interativamente como o usuário especificado no parâmetro \_ \_ \_ \_ *user.*  

</dd> <dt>

*runningTask* \[ out\]
</dt> <dd>

Um [**objeto RunningTask**](runningtask.md) que define a nova instância da tarefa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método retornará sem erro, mas a tarefa não será executado se a propriedade [**TaskSettings.AllowDemandStart**](tasksettings-allowdemandstart.md) estiver definida como false para a tarefa registrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





