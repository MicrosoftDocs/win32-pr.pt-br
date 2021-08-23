---
description: Especifica informações sobre uma rede de celular.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Tipo complexo providerType (banda larga móvel)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: eb62fbb55f83d004f70093fbde974f8ab08e6367742f34dbf166d1c25a63b28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975055"
---
# <a name="providertype-complex-type"></a>Tipo complexo providerType

O tipo complexo **ProviderType** especifica informações sobre uma rede de celular.

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                          | Type                                                           | Descrição               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [**ProviderID**](schema-providerid-providertype-element.md)     | [**providerIdType**](schema-provideridtype-simpletype.md)     | ID do provedor.<br/>   |
| [**ProviderName**](schema-providername-providertype-element.md) | [**providerNametype**](schema-providernametype-simpletype.md) | Nome do provedor.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




