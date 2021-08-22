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
ms.openlocfilehash: 85f20b364998fb34f3fe9eb6973770b414de501b60e34df6f97a607acb494947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118588175"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**evento**](eventschema-event-element.md)
</dt> </dl>

 

 





