---
title: Elemento data (comhandletype)
description: Especifica dados adicionais associados ao manipulador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Agendador de Tarefas de elemento de dados
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918903"
---
# <a name="data-comhandlertype-element"></a>Elemento data (comhandletype)

Especifica dados adicionais associados ao manipulador.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

O elemento de **dados** é definido pelo tipo complexo [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                             | Descrição                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md) | Especifica uma ação que dispara um manipulador.<br/> |



## <a name="remarks"></a>Comentários

Os aplicativos definem os dados do manipulador usando a propriedade [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) da interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





