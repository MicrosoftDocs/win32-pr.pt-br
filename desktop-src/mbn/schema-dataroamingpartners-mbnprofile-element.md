---
description: Especifica a lista de provedores de rede preferenciais no momento do roaming.
ms.assetid: 5873fcd7-8e89-4edd-8dc5-f43675919c55
title: Elemento DataRoamingPartners (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DataRoamingPartners
api_type:
- Schema
ms.openlocfilehash: 7f721abd608dd241c399f16eee90369ebcf19594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811240"
---
# <a name="dataroamingpartners-mbnprofile-element"></a>Elemento DataRoamingPartners (MBNProfile)

O elemento **DataRoamingPartners (MBNProfile)** especifica a lista de provedores de rede preferenciais no momento do roaming.

O serviço de banda larga móvel usa esse elemento para selecionar a rede preferencial fornecida durante o roaming.

O elemento tem o seguinte elemento filho que deve ser definido pelo menos uma vez, mas pode ser definido várias vezes.

-   [**Provedor**](schema-provider-dataroamingpartners-element.md)

Esse elemento pode ter um máximo de uma ocorrência.

Esse elemento é opcional.

``` syntax
<xs:element name="DataRoamingPartners">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Provider"
                type="providerType"
                maxOccurs="unbounded"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

O elemento **DataRoamingPartners** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                         | Type                                                    | Descrição                                            |
|-----------------------------------------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| [**Provedor**](schema-provider-dataroamingpartners-element.md) | [**providerType**](schema-providertype-complextype.md) | Nome e ID de provedor de uma rede de celular.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




