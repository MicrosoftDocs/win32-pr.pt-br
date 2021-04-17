---
description: Especifica o nome e o tipo de uma rede sem fio.
ms.assetid: 839afae0-b8e1-489f-8811-19a82c173627
title: Tipo complexo networkitemtype
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkItemType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5db7c5fc4d9b5227d9cd29c5e2dfc69da6fad139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782183"
---
# <a name="networkitemtype-complex-type"></a>Tipo complexo networkitemtype

O tipo complexo networkitemtype especifica o nome e o tipo de uma rede sem fio.

``` syntax
<xs:complexType name="networkItemType">
    <xs:sequence>
        <xs:element name="networkName"
            type="networkNameType"
         />
        <xs:element name="networkType"
            type="networkTypeType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                      | Type                                                                    | Descrição                                                   |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------|
| [**networkName**](wlan-policyschema-networkname-networkitemtype-element.md) | [**networkNameType**](wlan-policyschema-networknametype-simpletype.md) | O SSID (identificador de conjunto de serviços) da rede. <br/> |
| [**NetworkType**](wlan-policyschema-networktype-networkitemtype-element.md) | [**networkTypeType**](wlan-policyschema-networktypetype-simpletype.md) | O tipo de rede. <br/>                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




