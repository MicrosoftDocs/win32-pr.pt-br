---
title: Tipo complexo PeapExtensionsTypeV2
description: Saiba mais sobre o tipo complexo PeapExtensionsTypeV2. Esse tipo permite aprimoramentos futuros no esquema.
ms.assetid: cb011182-afec-4813-bd56-add894c74c9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baea42ec60fe84085ea5e4541848fd43b786419bedab17e938044ff0a713fa07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086025"
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

 

 




