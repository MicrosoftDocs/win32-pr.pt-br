---
title: Tipo complexo PeapExtensionsTypeV2
description: Saiba mais sobre o tipo complexo PeapExtensionsTypeV2. Esse tipo permite aprimoramentos futuros no esquema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869e67f16bc9b42929d227755e08bf6924dcc737
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917691"
---
# <a name="peapextensionstypev2-complex-type"></a>Tipo complexo PeapExtensionsTypeV2

O tipo complexo **PeapExtensionsTypeV2** permite aprimoramentos futuros no esquema.


```XML
<xs:complexType name="PeapExtensionsTypeV2">
    <xs:sequence>
        <xs:any processContents="lax" 
            minOccurs="0" 
            maxOccurs="unbounded" 
            namespace="##other"
        />
    <xs:sequence>
</xs:complexType>

```



## <a name="remarks"></a>Comentários

O elemento **PeapExtensionsTypeV2** é opcional.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Tipos complexos mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> <dt>

[**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> </dl>

 

 




