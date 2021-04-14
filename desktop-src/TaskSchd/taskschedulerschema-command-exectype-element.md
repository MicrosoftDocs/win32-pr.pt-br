---
title: Elemento Command (exectype)
description: Especifica o arquivo ou documento executável a ser executado.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Elemento de comando Agendador de Tarefas
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369825"
---
# <a name="command-exectype-element"></a>Elemento Command (exectype)

Especifica o arquivo ou documento executável a ser executado.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

O elemento **Command** é definido pelo tipo complexo [**exectype**](taskschedulerschema-exectype-complextype.md) .

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

 

 





