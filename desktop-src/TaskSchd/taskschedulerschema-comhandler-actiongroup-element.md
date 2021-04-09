---
title: Elemento comhandlers (The actioner)
description: Especifica uma ação que dispara um manipulador.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Agendador de Tarefas de elemento do commanipulador
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918904"
---
# <a name="comhandler-actiongroup-element"></a>Elemento comhandlers (The actioner)

Especifica uma ação que dispara um manipulador.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

O elemento **commanipulador** é definido pelo The [**Action**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento pai



| Elemento                                                         | Derivado de                                                       | Descrição                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Ações**](taskschedulerschema-actions-tasktype-element.md) | [**ActionType**](taskschedulerschema-actionstype-complextype.md) | Contém as ações executadas pela tarefa.<br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type                                                         | Descrição                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidtype**](taskschedulerschema-guidtype-simpletype.md)  | Especifica o identificador da classe do manipulador.<br/>         |
| [**Dados**](taskschedulerschema-data-comhandlertype-element.md)       | [**Tipo de dados**](taskschedulerschema-datatype-complextype.md) | Especifica dados adicionais associados ao manipulador.<br/> |



## <a name="remarks"></a>Comentários

Os aplicativos definem uma ação de manipulador COM usando a interface [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

### <a name="attributes"></a>Atributos

O atributo a seguir é definido pelo tipo complexo [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .

-   ID: identificador da ação executada pela tarefa.

## <a name="examples"></a>Exemplos

O XML a seguir define uma ação de manipulador COM.


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos do esquema de Agendador de Tarefas](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





