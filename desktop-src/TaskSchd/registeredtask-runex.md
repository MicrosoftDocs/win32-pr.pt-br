---
title: Método RegisteredTask. RunEx
description: Para scripts, o executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.
ms.assetid: 427bb51b-ddb1-4e47-9313-297366ba5ab7
keywords:
- Agendador de Tarefas do método RunEx
- Método RunEx Agendador de Tarefas, objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas, método RunEx
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
ms.openlocfilehash: 1d88eb8bb651929c905f080f97a9eaefd3b4dace
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085883"
---
# <a name="registeredtaskrunex-method"></a>Método RegisteredTask. RunEx

Para scripts, o executa a tarefa registrada imediatamente usando sinalizadores especificados e um identificador de sessão.

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

*parâmetros* \[ no\]
</dt> <dd>

Os parâmetros usados como valores nas ações da tarefa. Para não especificar nenhum valor de parâmetro para as ações de tarefa, defina esse parâmetro como **Nothing**. Caso contrário, um único valor de cadeia de caracteres ou uma matriz de valores de cadeia de caracteres pode ser especificado.

Os valores de cadeia de caracteres que você especifica são emparelhados com nomes e armazenados como pares de nome-valor. Se você especificar um único valor de cadeia de caracteres, Arg0 será o nome atribuído ao valor. O valor pode ser usado na ação da tarefa em que a variável $ (Arg0) é usada nas propriedades da ação.

Se você passar valores como "0", "100" e "250" como uma matriz de valores de cadeia de caracteres, "0" substituirá as variáveis $ (Arg0), "100" substituirá as variáveis $ (arg1) e "250" substituirá as variáveis $ (arg2) usadas nas propriedades da ação.

Um máximo de 32 valores de cadeia de caracteres podem ser especificados.

Para obter mais informações e uma lista de propriedades de ação que podem usar as variáveis $ (Arg0), $ (arg1),..., $ (Arg32) em seus valores, consulte [ações de tarefas](task-actions.md).

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Uma constante de [ \_ \_ sinalizadores de execução de tarefa](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags) que define como a tarefa é executada.

</dd> <dt>

*SessionID* \[ no\]
</dt> <dd>

A sessão do Terminal Server na qual você deseja iniciar a tarefa.

Se a execução da tarefa \_ \_ usar \_ constante de ID de sessão \_ (0x4) não for passada para o parâmetro *flags* , o valor especificado nesse parâmetro será ignorado. Se a execução da tarefa \_ \_ usar \_ \_ constante de ID de sessão for passada para o parâmetro *flags* e o valor SessionID for menor ou igual a 0, um erro de argumento inválido será retornado.

Se a execução da tarefa \_ \_ usar \_ constante de ID de sessão \_ for passada para o parâmetro *flags* e o valor SessionID for uma ID de sessão válida maior que 0 e se nenhum valor for especificado para o parâmetro *User* , o serviço de Agendador de tarefas tentará iniciar a tarefa interativamente como o usuário que fez logon na sessão especificada.

Se a execução da tarefa \_ \_ usar \_ constante de ID de sessão \_ for passada para o parâmetro *flags* e o valor SessionID for uma ID de sessão válida maior que 0 e se um usuário for especificado no parâmetro *User* , o serviço de Agendador de tarefas tentará iniciar a tarefa interativamente como o usuário que é especificado no parâmetro *User* .

</dd> <dt>

*runningTask* \[ fora\]
</dt> <dd>

Um objeto [**RunningTask**](runningtask.md) que define a nova instância da tarefa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método retornará sem erro, mas a tarefa não será executada se a propriedade [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md) for definida como false para a tarefa registrada.

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

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





