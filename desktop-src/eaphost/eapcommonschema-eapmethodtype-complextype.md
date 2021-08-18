---
title: Tipo complexo EapMethodType
description: Define os elementos que identificam exclusivamente um único tipo de método EAP, VendorID, VendorID e AuthorId.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType tipo complexo EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 059ea8162241c61d88fc93f565fa0aa4ba8aee223212e6fab254ed9d5dec4eea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739166"
---
# <a name="eapmethodtype-complex-type"></a>Tipo complexo EapMethodType

O tipo complexo **EapMethodType** define os elementos que identificam exclusivamente um único método EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md)e [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Type**](eapcommonschema-type-eapmethodtype-element.md) e [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) são elementos obrigatórios, enquanto [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) são necessários somente quando o elemento **Type** é 254 (um método EAP expandido).

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                | Type         | Descrição                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Refere-se ao autor do método. <br/>                                                                                                                                                                                                                 |
| [**Tipo**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Refere-se ao tipo de método EAP. <br/>                                                                                                                                                                                                               |
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Refere-se ao fornecedor que definiu o método – se o elemento [**Type**](eapcommonschema-type-eapmethodtype-element.md) for 254 (um método EAP expandido). O [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) é opcional. <br/> |
| [**Nome_do_Fornecedor**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | É o tipo definido pelo fornecedor para o método. O [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md) é opcional. <br/>                                                                                                           |



## <a name="remarks"></a>Comentários

Os elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) não precisam ser os mesmos para um método específico.

Os elementos [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) e [**VendorName**](eapcommonschema-vendortype-eapmethodtype-element.md) são cada um deles um número exclusivo emitido pela IANA (Internet Assigned Numbers Authority).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





