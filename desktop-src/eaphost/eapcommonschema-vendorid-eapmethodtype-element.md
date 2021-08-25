---
title: Elemento VendorId (EapMethodType)
description: Refere-se ao fornecedor que definiu o método se o elemento Type (EapMethodType) for 254 (um método EAP expandido).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento VendorId EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29508121a9724a52df19038b82d97576a924c3c8bab49ac6801c1de51ec71919
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067296"
---
# <a name="vendorid-eapmethodtype-element"></a>Elemento VendorId (EapMethodType)

O **elemento VendorId (EapMethodType)** refere-se ao fornecedor que definiu o método se o elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) for 254 (um método EAP expandido).

O **VendorId** é opcional. Se usado, **VendorId** é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

O **elemento VendorId** é definido pelo tipo complexo [**EapMethodType.**](eapcommonschema-eapmethodtype-complextype.md)

## <a name="remarks"></a>Comentários

Os [**elementos AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) e **VendorId** não precisam ser os mesmos para um método específico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





