---
title: Método RegisteredTask.Run
description: Para scripts, executa a tarefa registrada imediatamente.
ms.assetid: 99c8f6ea-6dcf-4f9a-bf61-5191df5958c6
keywords:
- Executar o método Agendador de Tarefas
- Executar método Agendador de Tarefas , objeto RegisteredTask
- Objeto RegisteredTask Agendador de Tarefas , método Run
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
ms.openlocfilehash: e747688ba80c08a39b0336fda126ae7d85a558f53c97aab230bc5d3d0113b360
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681616"
---
# <a name="registeredtaskrun-method"></a>Método RegisteredTask.Run

Para scripts, executa a tarefa registrada imediatamente.

## <a name="syntax"></a>Sintaxe


```VB
RegisteredTask.Run( _
  ByVal params, _
  ByRef ppRunningTask _
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

*ppRunningTask* \[ out\]
</dt> <dd>

Um [**objeto RunningTask**](runningtask.md) que define a nova instância da tarefa.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A **função RegisteredTask.Run** é equivalente à função [**RegisteredTask.RunEx**](registeredtask-runex.md) com o parâmetro flags igual a 0 e nada especificado para o parâmetro de usuário.

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

 

 





