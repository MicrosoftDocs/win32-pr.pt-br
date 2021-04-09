---
description: Identifica o nome e a ID do provedor para uma rede de celular.
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
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090301"
---
# <a name="provider-dataroamingpartners-element"></a>Elemento Provider (DataRoamingPartners)

O elemento **Provider (DataRoamingPartners)** identifica o nome e a ID do provedor para uma rede de celular.

Este elemento tem os seguintes elementos filho.

-   [**ProviderID**](schema-providerid-providertype-element.md)
-   [**ProviderName**](schema-providername-providertype-element.md)

Esse elemento pode ser definido várias vezes dentro do elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) . Ele deve ser definido pelo menos uma vez.

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

O elemento **Provider** é definido pelo elemento [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
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

 

 




