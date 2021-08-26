---
title: Elemento timecriado (SystemPropertiesType)
description: O carimbo de data/hora que identifica quando o evento foi registrado.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- EventLog de elemento TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5026bed56e3e065a403c0e6076daa0ec478223c4d742db0a35109a41cc98d5c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005296"
---
# <a name="timecreated-systempropertiestype-element"></a>Elemento timecriado (SystemPropertiesType)

O carimbo de data/hora que identifica quando o evento foi registrado.

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

O elemento **Timecriated** é definido pelo tipo complexo [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome       | Tipo     | Descrição                                              |
|------------|----------|----------------------------------------------------------|
| SystemTime | dateTime | A hora do sistema de quando o evento foi registrado.<br/> |



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

 

 





