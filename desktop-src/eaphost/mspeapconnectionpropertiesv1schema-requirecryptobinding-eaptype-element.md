---
title: Elemento RequireCryptoBinding (EapType)
description: Indica se é necessário autenticar com servidores que suportam a criptografia.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Elemento RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c4f4169e6ac0af123085795374b06de854b261b5f22004bd726ad47488bc11d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067216"
---
# <a name="requirecryptobinding-eaptype-element"></a>Elemento RequireCryptoBinding (EapType)

O **elemento RequireCryptoBinding (EapType)** indica se é necessário autenticar com servidores que suportam criptografia.

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

O **elemento RequireCryptoBinding** é definido pelo [**elemento EapType.**](mspeapconnectionpropertiesv1schema-eaptype-element.md)

## <a name="remarks"></a>Comentários

Se o **elemento RequireCryptoBinding** for TRUE, o PEAP será autenticado com servidores que não têm suporte para criptografia. se FALSE, o PEAP só será autenticado com servidores que deem suporte à criptografia. O **elemento RequireCryptoBinding** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





