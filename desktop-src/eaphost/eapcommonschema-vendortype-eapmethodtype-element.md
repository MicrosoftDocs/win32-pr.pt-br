---
title: Elemento Vendor (EapMethodType)
description: Saiba mais sobre o elemento Vendor (EapMethodType). Esse elemento é o tipo definido pelo fornecedor para o método.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Elemento VendorID do Vendor
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454340"
---
# <a name="vendortype-eapmethodtype-element"></a>Elemento Vendor (EapMethodType)

O elemento **Vendor (EapMethodType)** é o tipo definido pelo fornecedor para o método.

O elemento **VendorID** é opcional. Se usado, o **VendorName** é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

O elemento **VendorID** é definido pelo tipo complexo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 





