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
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164574"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/> |
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

 

 




