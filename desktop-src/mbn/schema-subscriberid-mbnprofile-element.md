---
description: Identifica o identificador exclusivo do perfil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Elemento subscriberid (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501844"
---
# <a name="subscriberid-mbnprofile-element"></a>Elemento subscriberid (MBNProfile)

O elemento **subscriberid (MBNProfile)** identifica o identificador exclusivo do perfil.

Para uma rede GSM, isso deve conter a IMSI (identidade do assinante internacional móvel) do SIM e para dispositivos CDMA que ele deve conter o mínimo (número de identificação móvel) do dispositivo.

O elemento é uma cadeia de caracteres numérica com um comprimento máximo de 15 dígitos.

O elemento é obrigatório.

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

O elemento **subscriberid** é definido pelo elemento [**MBNProfile**](schema-mbnprofile-element.md) .

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

 

 




