---
title: Elemento binary (TemplateItemType)
description: Contém os dados binários fornecidos pela API do log de eventos.
ms.assetid: 3ad9c119-9395-49d3-b920-9a071bcc6a04
keywords:
- elemento Binary EventLog
topic_type:
- apiref
api_name:
- binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c3e281da662b4cdd0ecacc81a88f1a5728f90da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763141"
---
# <a name="binary-templateitemtype-element"></a>Elemento binary (TemplateItemType)

Contém os dados binários fornecidos pela API do [log de eventos](/windows/desktop/EventLog/event-logging) .

``` syntax
<xs:element name="binary">
    <xs:complexType>
        <xs:attribute name="name"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O elemento **Binary** é definido pelo tipo complexo [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                          |
|------|--------|------------------------------------------------------|
| name | string | O nome associado aos dados binários.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**modelo (TemplateListType)**](eventmanifestschema-template-templatelisttype-element.md)
</dt> </dl>

 

