---
title: Elemento EapType (mspeapconnectionpropertiesv1schema)
description: Esse elemento é um tipo derivado do elemento EapType do esquema BaseEapConnectionProperties. Para mspeapconnectionpropertiesv1schema.
ms.assetid: 13238968-f3ef-4e9c-a525-d1f6efbaee0d
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
ms.openlocfilehash: 47f3585f35b2e7ee7722cdd99c90605cdb7864b2211fcf28f7ec0ac662b5289b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719767"
---
# <a name="eaptype-element-mspeapconnectionpropertiesv1schema"></a>Elemento EapType (mspeapconnectionpropertiesv1schema)

O **elemento EapType** é um tipo derivado do elemento [**EapType**](baseeapconnectionpropertiesv1schema-eaptype-element.md) do [esquema BaseEapConnectionProperties.](baseeapconnectionpropertiesv1schema-schema.md)

Esse elemento **EapType** derivado contém os seguintes elementos: [**ServerValidation,**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) [**IdentityPrivacy,**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) [**FastReconnect,**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) [**InnerEapOptional,**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md), [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md), [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) e [**PeapExtensions.**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)

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
                    <xs:element name="ServerValidation"
                        type="ServerValidationParameters"
                        minOccurs="0"
                     />
                    <xs:element name="IdentityPrivacy"
                        type="IdentityPrivacyParameters"
                        minOccurs="0"
                     />
                    <xs:element name="FastReconnect"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element name="InnerEapOptional"
                        type="boolean"
                        minOccurs="0"
                     />
                    <xs:element
                        minOccurs="0"
                        maxOccurs="unbounded"
                        ref="Eap"
                     />
                    <xs:element name="EnableQuarantineChecks"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="RequireCryptoBinding"
                        type="boolean"
                        default="false"
                        minOccurs="0"
                     />
                    <xs:element name="PeapExtensions"
                        type="PeapExtensionsType"
                        minOccurs="0"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                     | Type                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md)                                              |                                                                                                                 | Descreve o método interno e a configuração do método. Se o [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) for TRUE, o [**elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar presente. Se o [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) for FALSE, o [**elemento Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar ausente.<br/>           |
| [**EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) | booleano                                                                                                         | Indica se é preciso executar verificações nap (proteção de acesso à rede). Se o [**elemento EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) for TRUE, o PEAP executará verificações NAP; se FALSE PEAP não executar verificações NAP. O [**elemento EnableQuarantineChecks**](mspeapconnectionpropertiesv1schema-enablequarantinechecks-eaptype-element.md) é opcional.<br/>                                                                                |
| [**FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md)                   | booleano                                                                                                         | Indica se é preciso executar uma reconexão rápida. Se o [**elemento FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) for TRUE, o PEAP tentará executar uma reconexão rápida; se FALSE, PEAP executará a autenticação completa. O [**elemento FastReconnect**](mspeapconnectionpropertiesv1schema-fastreconnect-eaptype-element.md) é opcional.<br/>                                                                                                                       |
| [**IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)          | [**IdentityPrivacyParameters**](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)         | Windows 7 ou posterior: indica se a identidade verdadeira de um usuário ou uma identidade anônima é enviada. O [**elemento IdentityPrivacy**](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md) é opcional.<br/>                                                                                                                                                                                                                                                                                 |
| [**InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md)             | booleano                                                                                                         | Indica se é preciso executar o acesso CONVIDADO. Se o [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) for TRUE, o elemento [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar presente e descrever o método interno e sua configuração; se FALSE, o PEAP executará o acesso CONVIDADO. O [**elemento InnerEapOptional**](mspeapconnectionpropertiesv1schema-innereapoptional-eaptype-element.md) é opcional.<br/>            |
| [**PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)                 | [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)                 | O [**elemento PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) permite aprimoramentos futuros para o esquema. O [**elemento PeapExtensions**](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md) é opcional.<br/>                                                                                                                                                                                                                                    |
| [**RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md)     | booleano                                                                                                         | Indica se é necessário autenticar com servidores que suportam a criptografia. Se o [**elemento RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) for TRUE, o PEAP será autenticado com servidores que não têm suporte para criptografia. se FALSE, o PEAP só será autenticado com servidores que deem suporte à criptografia. O [**elemento RequireCryptoBinding**](mspeapconnectionpropertiesv1schema-requirecryptobinding-eaptype-element.md) é opcional.<br/> |
| [**ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)             | [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) | Contém informações sobre como executar a validação do servidor. O [**elemento ServerValidation**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md) é opcional.<br/>                                                                                                                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos de esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





