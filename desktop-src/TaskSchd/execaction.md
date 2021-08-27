---
title: Objeto execaction
description: Objeto de script que representa uma ação que executa uma operação de linha de comando.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- executar Agendador de Tarefas de ação, interface
- Agendador de Tarefas de objeto execaction
- Agendador de Tarefas de objeto execaction, descrito
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140ff991bd26f779beee7407666572d8649bd9f1a2718b719713770745157656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072656"
---
# <a name="execaction-object"></a>Objeto execaction

Objeto de script que representa uma ação que executa uma operação de linha de comando.

## <a name="members"></a>Membros

O objeto **execaction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **execaction** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso           | Descrição                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Leitura/gravação<br/> | Obtém ou define os argumentos associados à operação de linha de comando.<br/>                                                 |
| [**Sessão**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Leitura/gravação<br/> | Herdado do objeto de [**ação**](action.md) . Obtém ou define o identificador da ação.<br/>                         |
| [**Caminho**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Leitura/gravação<br/> | Obtém ou define o caminho para um arquivo executável.<br/>                                                                           |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Somente leitura<br/>  | Herdado do objeto de [**ação**](action.md) . Obtém o tipo da ação.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Leitura/gravação<br/> | Obtém ou define o diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.<br/> |



 

## <a name="remarks"></a>Comentários

Se as variáveis de ambiente forem usadas nas propriedades [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)ou [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , os valores das variáveis de ambiente serão armazenados em cache e usados quando a Taskeng.exe (o mecanismo de tarefa) for iniciada. As alterações nas variáveis de ambiente que ocorrem após a inicialização do mecanismo de tarefa não serão usadas pelo mecanismo de tarefa.

Essa ação executa uma operação de linha de comando. Por exemplo, a ação pode executar um script ou iniciar um executável.

Ao ler ou gravar XML, uma ação de execução é especificada no elemento [**exec**](taskschedulerschema-exec-actiongroup-element.md) do esquema de Agendador de tarefas.

## <a name="examples"></a>Exemplos

Para obter mais informações e código de exemplo para esse objeto de script, consulte [exemplo de gatilho de tempo (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Biblioteca de tipos<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





