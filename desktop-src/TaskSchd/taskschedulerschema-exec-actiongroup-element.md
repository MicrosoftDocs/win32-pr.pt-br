---
title: Elemento exec (actionproperty)
description: Especifica uma ação que executa uma operação de linha de comando.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Agendador de Tarefas do elemento exec
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810114"
---
# <a name="exec-actiongroup-element"></a>Elemento exec (actionproperty)

Especifica uma ação que executa uma operação de linha de comando.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

O elemento **exec** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                         | Derivado de                                                       | Descrição                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md) | [**ActionType**](taskschedulerschema-actionstype-complextype.md) | Contém as ações executadas pela tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                           | Type       | Descrição                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Argumentos**](taskschedulerschema-arguments-exectype-element.md)               | **cadeia de caracteres** | Especifica os argumentos associados à operação de linha de comando.<br/>                               |
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | **cadeia de caracteres** | Especifica o arquivo ou documento executável a ser executado.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | string     | Especifica o diretório em que o executável ou os arquivos usados pelo executável existem.<br/> |



## <a name="attributes"></a>Atributos



| Nome | Tipo       | Descrição                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **cadeia de caracteres** | O identificador da ação executada pela tarefa.<br/> |



## <a name="remarks"></a>Comentários

Os elementos filho listados acima são definidos pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .

Para o desenvolvimento de script, uma ação de execução é definida pelo objeto [**execaction**](execaction.md) .

Para desenvolvimento em C++, uma ação de execução é definida pela interface [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .

Se as variáveis de ambiente forem usadas nos elementos [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)ou [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , os valores das variáveis de ambiente serão armazenados em cache e usados quando a Taskeng.exe (o mecanismo de tarefa) for iniciada. As alterações nas variáveis de ambiente que ocorrem após a inicialização do mecanismo de tarefa não serão usadas pelo mecanismo de tarefa.

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa um gatilho de evento, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





