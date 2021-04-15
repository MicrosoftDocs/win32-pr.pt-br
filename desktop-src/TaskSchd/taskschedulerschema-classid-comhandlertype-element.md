---
title: Elemento ClassID (comhandletype)
description: Especifica o identificador da classe do manipulador.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- Elemento ClassID Agendador de Tarefas
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455987"
---
# <a name="classid-comhandlertype-element"></a>Elemento ClassID (comhandletype)

Especifica o identificador da classe do manipulador.

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

O elemento **ClassID** é definido pelo tipo complexo [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                                  | Derivado de                                                             | Descrição                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [**Commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md) | [**comhandletype**](taskschedulerschema-comhandlertype-complextype.md) | Especifica uma ação que dispara um manipulador.<br/> |



## <a name="remarks"></a>Comentários

Os aplicativos definem o identificador de classe usando a propriedade [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) da interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





