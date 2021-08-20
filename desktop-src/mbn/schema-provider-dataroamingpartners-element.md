---
description: Identifica o nome e a ID do provedor de uma rede celular.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Elemento Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: d5ce12ddf15ad57071f2717e5801fbd05f8e2925ea474345f7c376bc2445cd02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119347156"
---
# <a name="provider-dataroamingpartners-element"></a>Elemento Provider (DataRoamingPartners)

O **elemento Provider (DataRoamingPartners)** identifica o nome e a ID do provedor para uma rede celular.

Esse elemento tem os seguintes elementos filho.

-   [**Providerid**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Esse elemento pode ser definido várias vezes dentro do [**elemento DataRoamingPartners.**](schema-dataroamingpartners-mbnprofile-element.md) Ele deve ser definido pelo menos uma vez.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

O **elemento** Provider é definido pelo [**elemento DataRoamingPartners.**](schema-dataroamingpartners-mbnprofile-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**DataRoamingPartners (MBNProfile)**](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




