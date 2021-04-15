---
title: Elemento do sistema (EventType)
description: Contém informações que identificam o provedor e como ele foi habilitado, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- Log de elemento do sistema
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761503"
---
# <a name="system-eventtype-element"></a>Elemento do sistema (EventType)

Contém informações que identificam o provedor e como ele foi habilitado, o evento, o canal no qual o evento foi gravado e informações do sistema, como as IDs de processo e thread.

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

O elemento **System** é definido pelo tipo complexo [**EventType**](eventschema-eventtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**evento**](eventschema-event-element.md)
</dt> </dl>

 

 





