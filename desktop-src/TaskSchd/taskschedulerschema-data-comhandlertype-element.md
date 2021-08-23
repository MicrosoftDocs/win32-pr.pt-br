---
title: Elemento Data (comHandlerType)
description: Especifica dados adicionais associados ao manipulador.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Elemento data Agendador de Tarefas
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 649cadf0fc10919902e65ce82df1b410708d74a9db8dd3638c6fb22753aa557a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334586"
---
# <a name="data-comhandlertype-element"></a>Elemento Data (comHandlerType)

Especifica dados adicionais associados ao manipulador.

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

O **elemento Data** é definido pelo tipo complexo [**comHandlerType.**](taskschedulerschema-comhandlertype-complextype.md)

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                             | Description                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) | Especifica uma ação que dispara um manipulador.<br/> |



## <a name="remarks"></a>Comentários

Os aplicativos definem os dados do manipulador [**usando a propriedade Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) da interface [**IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Agendador de Tarefas de esquema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





