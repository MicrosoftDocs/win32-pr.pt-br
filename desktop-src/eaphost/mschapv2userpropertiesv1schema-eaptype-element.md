---
title: Elemento EapType (mschapv2userpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema baseeapuserpropertiesv1. Para o mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187747"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a>Elemento EapType (mschapv2userpropertiesv1schema)

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
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



| Elemento                                                                           | Type   | Descrição                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Usu**](mschapv2userpropertiesv1schema-username-element.md)               |        | Identifica o usuário que está sendo autenticado. Se esse elemento não estiver presente, o nome de usuário será obtido do Winlogon. O elemento [**username**](mschapv2userpropertiesv1schema-username-element.md) é opcional.<br/>                                        |
| [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | string | Identifica o domínio do usuário ou computador que está sendo autenticado. Se esse elemento não estiver presente, o domínio do Winlogon será usado. O elemento [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) é opcional.<br/>        |
| [**Senha**](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | string | Identifica a senha do usuário ou computador que está sendo autenticado. Se esse elemento não estiver presente, o hash de senha será obtido do Winlogon. O elemento [**password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) é opcional.<br/> |



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

[Esquema mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





