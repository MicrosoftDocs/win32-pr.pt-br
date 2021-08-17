---
description: Especifica a ID do provedor da rede de celular.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: Elemento ProviderId (providerType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: b40ac5abab2abf850d927c21f0de66ad419987f594f28dffcd380ead7f982d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959786"
---
# <a name="providerid-providertype-element"></a>Elemento ProviderId (providerType)

O elemento **ProviderId (ProviderType)** especifica a ID do provedor da rede de celular.

O elemento é uma sequência de dígitos com um máximo de 6 dígitos.

Esse elemento é necessário dentro do elemento [**Provider**](schema-provider-dataroamingpartners-element.md) .

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

O elemento **ProviderID** é definido pelo tipo complexo [**ProviderType**](schema-providertype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**providerType**](schema-providertype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Provedor (DataRoamingPartners)**](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




