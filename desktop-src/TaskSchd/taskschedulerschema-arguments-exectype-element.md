---
title: Elemento Arguments (execType)
description: Especifica os argumentos associados à operação de linha de comando.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Elemento Arguments Agendador de Tarefas
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edf76f7073e62aac10c85dc035d3b441a90a4e0ee1fae90b4decf5cffc4568df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132071"
---
# <a name="arguments-exectype-element"></a>Elemento Arguments (execType)

Especifica os argumentos associados à operação de linha de comando.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

O **elemento Arguments** é definido pelo [**tipo complexo execType.**](taskschedulerschema-exectype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                      | Derivado de                                                 | Descrição                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Especifica uma ação que executa uma operação de linha de comando.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**propriedade Arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Para desenvolvimento de scripts, [**consulte ExecAction.Arguments.**](execaction-arguments.md)

## <a name="examples"></a>Exemplos

Para ver um exemplo completo do XML para uma tarefa que usa uma ação executável, consulte Exemplo [de gatilho de tempo (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





