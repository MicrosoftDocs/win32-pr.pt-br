---
title: Método RegisteredTask. Run
description: Para scripts, o executa a tarefa registrada imediatamente.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Agendador de Tarefas do método de execução
- Método Run Agendador de Tarefas, objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, método Run
topic_type:
- apiref
api_name:
- RegisteredTask.Run
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd10539518b22f596e42afd56324c90b881412b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810990"
---
# <a name="registeredtaskrun-method"></a>Método RegisteredTask. Run

Para scripts, o executa a tarefa registrada imediatamente.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
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

*ppRunningTask* \[ fora\]
</dt> <dd>

Um objeto [**RunningTask**](runningtask.md) que define a nova instância da tarefa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A função **RegisteredTask. Run** é equivalente à função [**RegisteredTask. RunEx**](registeredtask-runex.md) com o parâmetro flags igual a 0 e nada especificado para o parâmetro User.

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

 

 





