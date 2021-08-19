---
title: Elemento AuthorId (EapMethodType)
description: Saiba mais sobre o elemento AuthorId (EapMethodType). O elemento AuthorID (EapMethodType) refere-se ao autor do método.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Elemento AuthorId EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f15c5fc981592bb82f9ad52d590f12ac0b1f4b20af3537a511d01dd0a8cc15e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021746"
---
# <a name="authorid-eapmethodtype-element"></a>Elemento AuthorId (EapMethodType)

O **elemento AuthorId (EapMethodType)** refere-se ao autor do método.

A AuthorId é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

O **elemento AuthorId** é definido pelo tipo complexo [**EapMethodType.**](eapcommonschema-eapmethodtype-complextype.md)

## <a name="remarks"></a>Comentários

Os **elementos AuthorId** e [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) não precisam ser os mesmos para um método específico.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



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

 

 





