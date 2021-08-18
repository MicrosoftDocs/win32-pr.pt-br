---
title: Objeto RepetitionPattern
description: Objeto de script que define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- disparadores Agendador de Tarefas, objeto de padrão de repetição
- padrão de repetição Agendador de Tarefas, objeto
- Agendador de Tarefas de objeto RepetitionPattern
- Agendador de Tarefas de objeto RepetitionPattern, descrito
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06583aaef7f41a2752ace9c67599c1d299b72f87cb9984674994ede10d89525b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872387"
---
# <a name="repetitionpattern-object"></a>Objeto RepetitionPattern

Objeto de script que define com que frequência a tarefa é executada e por quanto tempo o padrão de repetição é repetido depois que a tarefa é iniciada.

## <a name="members"></a>Membros

O objeto **RepetitionPattern** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **RepetitionPattern** tem essas propriedades.



| Propriedade                                                                    | Tipo de acesso           | Descrição                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Permanência**](repetitionpattern-duration.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define por quanto tempo o padrão é repetido.<br/>                                                                                          |
| [**Intervalo**](repetitionpattern-interval.md)<br/>                   | Leitura/gravação<br/> | Obtém ou define o período de tempo entre cada reinicialização da tarefa.<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | Leitura/gravação<br/> | Obtém ou define um valor booliano que indica se uma instância em execução da tarefa é interrompida no final da duração do padrão de repetição.<br/> |



 

## <a name="remarks"></a>Comentários

Se você especificar uma duração de repetição para uma tarefa, também deverá especificar o intervalo de repetição.

Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada cinco vezes. As cinco repetições podem ser definidas pelo padrão a seguir.

1.  Uma tarefa é iniciada no início do primeiro minuto.
2.  A próxima tarefa é iniciada no final do primeiro minuto.
3.  A próxima tarefa é iniciada no final do segundo minuto.
4.  A próxima tarefa começa no final do terceiro minuto.
5.  A próxima tarefa é iniciada no final do quarto minuto.

**Windows Server 2003, Windows XP e Windows 2000:** Se você registrar uma tarefa que contém um gatilho com um intervalo de repetição igual a um minuto e uma duração de repetição igual a quatro minutos, a tarefa será iniciada quatro vezes.

Ao ler ou gravar XML em uma tarefa, o padrão de repetição é especificado usando o elemento de [**repetição**](taskschedulerschema-repetition-triggerbasetype-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para essa propriedade, consulte [exemplo de gatilho diário (script)](daily-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos Agendador de Tarefas](task-scheduler-objects.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





