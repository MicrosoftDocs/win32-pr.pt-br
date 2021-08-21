---
title: Elemento EapType (mschapv2connectionpropertiesv1schema)
description: É um tipo derivado do elemento EapType do esquema baseeapconnectionpropertiesv1. Esse é o elemento superior que aparece dentro do elemento config do esquema EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 18d3296dfab4a28ba818199d0b9329888c692f55831bced2af5abedfd1f205e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984056"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a>Elemento EapType (mschapv2connectionpropertiesv1schema)

O elemento **EapType** é um tipo derivado do elemento [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) do esquema [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) . Esse é o elemento superior que aparece dentro do elemento config do esquema [EapHostConfig](eaphostconfigschema-elements.md)

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
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



| Elemento                                                                                                       | Type    | Descrição                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UseWinLogonCredentials**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | booleano | Controla o uso das credenciais Winlogin. Se for TRUE, o EAP MS-CHAPv2 obterá as credenciais do Winlogon. Se for FALSE, o EAP MS-CHAPv2 obterá as credenciais do usuário. <br/> O elemento [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) é opcional.<br/> |



## <a name="remarks"></a>Comentários

O elemento **ProcessContents** permite aprimoramentos futuros no esquema. O elemento **ProcessContents** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





