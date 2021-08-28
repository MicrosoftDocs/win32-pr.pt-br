---
title: Elemento Exec (actionGroup)
description: Especifica uma ação que executa uma operação de linha de comando.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Elemento Exec Agendador de Tarefas
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 709cded1238654fffcf8ce75e5cba85c6139eb6264592e99684462e0a9cb2661
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072486"
---
# <a name="exec-actiongroup-element"></a>Elemento Exec (actionGroup)

Especifica uma ação que executa uma operação de linha de comando.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

O **elemento Exec** é definido pelo [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                         | Derivado de                                                       | Descrição                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contém as ações executadas pela tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type       | Descrição                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](taskschedulerschema-arguments-exectype-element.md)               | **cadeia de caracteres** | Especifica os argumentos associados à operação de linha de comando.<br/>                               |
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | **cadeia de caracteres** | Especifica o arquivo executável ou o documento a ser executado.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | string     | Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo       | Descrição                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **cadeia de caracteres** | O identificador da ação executada pela tarefa.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho listados acima são definidos pelo [**tipo complexo execType.**](taskschedulerschema-exectype-complextype.md)

Para desenvolvimento de script, uma ação de execução é definida pelo [**objeto ExecAction.**](execaction.md)

Para o desenvolvimento em C++, uma ação de execução é definida pela interface [**IExecAction.**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)

Se as variáveis de ambiente são usadas nos elementos [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md)ou [**WorkingDirectory,**](taskschedulerschema-workingdirectory-exectype-element.md) os valores das variáveis de ambiente são armazenados em cache e usados quando o Taskeng.exe (o mecanismo de tarefas) é lançado. As alterações nas variáveis de ambiente que ocorrem depois que o mecanismo de tarefas é lançado não serão usadas pelo mecanismo de tarefas.

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que usa um gatilho de evento, consulte [Exemplo de gatilho de tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





