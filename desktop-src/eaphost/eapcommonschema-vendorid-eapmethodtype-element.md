---
title: Elemento Vendor (EapMethodType)
description: Refere-se ao fornecedor que definiu o método se o elemento Type (EapMethodType) for 254 (um método EAP expandido).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Elemento Vendor EAPHost
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
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499412"
---
# <a name="vendorid-eapmethodtype-element"></a>Elemento Vendor (EapMethodType)

O elemento **Vendor (EapMethodType)** refere-se ao fornecedor que definiu o método se o elemento [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) for 254 (um método EAP expandido).

O **VendorID** é opcional. Se usado, o **VendorID** é um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

O elemento **VendorID** é definido pelo tipo complexo [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .

## <a name="remarks"></a>Comentários

Os elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) e **VendorID** não precisam ser os mesmos para um método específico.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 





