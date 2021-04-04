---
title: Tipo complexo comhandletype
description: Define os elementos filho e as informações de sequenciamento para o elemento commanipulador.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- tipo complexo comhandletype Agendador de Tarefas
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009156"
---
# <a name="comhandlertype-complex-type"></a>Tipo complexo comhandletype

Define os elementos filho e as informações de sequenciamento para o elemento [**commanipulador**](taskschedulerschema-comhandler-actiongroup-element.md) .

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type                                                         | Descrição                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidtype**](taskschedulerschema-guidtype-simpletype.md)  | Especifica o identificador da classe do manipulador.<br/>          |
| [**Dados**](taskschedulerschema-data-comhandlertype-element.md)       | [**Tipo de dados**](taskschedulerschema-datatype-complextype.md) | Especifica dados adicionais associados ao manipulador. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos complexos de esquema de Agendador de Tarefas](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Agendador de Tarefas](task-scheduler-start-page.md)
</dt> </dl>

 

 





