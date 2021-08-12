---
title: Tipo complexo FilterListType
description: Define uma lista de filtros que um controlador ETW pode passar para seu provedor para limitar ainda mais os eventos que ele grava.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Tipo complexo FilterListType EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b66ccc002372159540895dfbe95786921266320bb4d3a4e6827085ae7822c12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118589621"
---
# <a name="filterlisttype-complex-type"></a>Tipo complexo FilterListType

Define uma lista de filtros que um controlador ETW pode passar para seu provedor para limitar ainda mais os eventos que ele grava.

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento    | Type                                                             | Descrição                   |
|------------|------------------------------------------------------------------|-------------------------------|
| **filter** | [**FilterType**](eventmanifestschema-filtertype-complextype.md) | Uma lista de filtros.<br/> |



## <a name="remarks"></a>Comentários

Um controlador ETW é um aplicativo que chama a [**função StartTrace**](/windows/desktop/ETW/starttrace) para criar uma sessão ETW. Para obter detalhes, consulte [Controlando sessões de rastreamento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions). O controlador pode usar a [**função TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) para enumerar os filtros que você define. Em seguida, o controlador pode passar um ou mais dos filtros quando chama a [**função EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) para habilitar o provedor. Seu provedor recebe os filtros, juntamente com o restante dos parâmetros enable, em sua função de retorno de chamada [*EnableCallback.*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

