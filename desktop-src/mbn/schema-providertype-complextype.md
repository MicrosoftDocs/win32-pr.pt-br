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
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754579"
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



| Elemento                                                          | Type                                                           | Description               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [**ProviderID**](schema-providerid-providertype-element.md)     | [**providerIdType**](schema-provideridtype-simpletype.md)     | ID do provedor.<br/>   |
| [**ProviderName**](schema-providername-providertype-element.md) | [**providerNametype**](schema-providernametype-simpletype.md) | Nome do provedor.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




