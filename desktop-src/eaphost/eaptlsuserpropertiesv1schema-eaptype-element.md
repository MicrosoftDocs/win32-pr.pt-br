---
title: Elemento EapType (eaptlsuserpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema baseeapuserpropertiesv1. Para o eaptlsuserpropertiesv1schema.
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187755"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a>Elemento EapType (eaptlsuserpropertiesv1schema)

O elemento **EapType** é um tipo derivado do elemento [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) do esquema [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                   | Type      | Descrição                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Usu**](eaptlsuserpropertiesv1schema-username-element.md)         |           | Captura o nome de usuário a ser enviado na resposta EAP-Identity. Se o elemento [**username**](eaptlsuserpropertiesv1schema-username-element.md) estiver ausente, o EAP-TLS usará o nome no certificado referido no elemento [**usercert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .<br/> |
| [**Usercert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | hexBinary | Refere-se ao hash SHA-1 do certificado que deve ser usado para autenticação.<br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a>Comentários

O elemento **ProcessContents** permite aprimoramentos futuros no esquema. O elemento **ProcessContents** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





