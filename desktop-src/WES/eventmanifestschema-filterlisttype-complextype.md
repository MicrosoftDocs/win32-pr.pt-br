---
title: Tipo complexo FilterListType
description: Define uma lista de filtros que um controlador ETW pode passar para seu provedor para limitar ainda mais os eventos que ele grava.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Log de eventos do tipo complexo FilterListType
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295891"
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

Um controlador ETW é um aplicativo que chama a função [**StartTrace**](/windows/desktop/ETW/starttrace) para criar uma sessão de ETW. Para obter detalhes, consulte [controlando sessões de rastreamento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions). O controlador pode usar a função [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) para enumerar os filtros que você definir. Em seguida, o controlador pode passar um ou mais dos filtros ao chamar a função [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) para habilitar seu provedor. Seu provedor recebe os filtros, juntamente com o restante dos parâmetros de habilitação, em sua função de retorno de chamada do [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

