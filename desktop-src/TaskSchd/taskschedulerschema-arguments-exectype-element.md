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
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499513"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





