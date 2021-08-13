---
title: Elemento Arguments (exectype)
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
# <a name="arguments-exectype-element"></a>Elemento Arguments (exectype)

Especifica os argumentos associados à operação de linha de comando.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

O elemento **arguments** é definido pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                      | Derivado de                                                 | Descrição                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**exectype**](taskschedulerschema-exectype-complextype.md) | Especifica uma ação que executa uma operação de linha de comando.<br/> |



## <a name="remarks"></a>Comentários

Para desenvolvimento em C++, consulte a [**Propriedade Arguments de IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Para desenvolvimento de script, consulte [**execaction. Arguments**](execaction-arguments.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo completo do XML para uma tarefa que usa uma ação executável, consulte [exemplo de gatilho de tempo (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





