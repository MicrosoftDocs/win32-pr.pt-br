---
title: Elemento de correlação (SystemPropertiesType)
description: Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Log de elementos de correlação
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc301c43bbc8ba834949ae2a5056fb4359b5c8db3125da3d1729b18ac7aa1b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118120354"
---
# <a name="correlation-systempropertiestype-element"></a>Elemento de correlação (SystemPropertiesType)

Os identificadores de atividade que os consumidores podem usar para agrupar eventos relacionados.

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

O elemento de **correlação** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome              | Tipo                                                | Descrição                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDtype**](eventschema-guidtype-simpletype.md) | Um identificador global exclusivo que identifica a atividade atual. Os eventos que são publicados com esse identificador fazem parte da mesma atividade.<br/>                              |
| RelatedActivityID | [**GUIDtype**](eventschema-guidtype-simpletype.md) | Um identificador global exclusivo que identifica a atividade para a qual o controle foi transferido. Em seguida, os eventos relacionados teriam esse identificador como seu identificador de ActivityId.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**Sistema (EventType)**](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





