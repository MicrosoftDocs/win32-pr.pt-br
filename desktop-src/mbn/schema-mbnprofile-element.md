---
description: É o elemento raiz que identifica um perfil de Banda Larga Móvel.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Elemento MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 049ec22c170afda3a46620e2e94e2a16ae2708b4d6a69fcd0262baa69352a0a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943356"
---
# <a name="mbnprofile-element"></a>Elemento MBNProfile

O **elemento MBNProfile** é o elemento raiz que identifica um perfil de Banda Larga Móvel.

Pode haver apenas um elemento desse tipo por documento.

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                          | Type                                                           | Descrição                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [**AutoConnectOnInternet**](schema-autoconnectoninternet-mbnprofile-element.md) | booleano                                                        | Se o dispositivo se conectará automaticamente.<br/> |
| [**ConnectionMode**](schema-connectionmode-mbnprofile-element.md)               |                                                                | As configurações de conexão automática do dispositivo.<br/>           |
| [**Contexto**](schema-context-mbnprofile-element.md)                             | [**contextType**](schema-contexttype-complextype.md)          | Parâmetros de configuração de conexão de dados.<br/>              |
| [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | Provedores de rede preferenciais para roaming.<br/>       |
| [**Descrição**](schema-description-mbnprofile-element.md)                     | [**nameType**](schema-nametype-simpletype.md)                 | Descrição do perfil.<br/>                    |
| [**HomeProviderName**](schema-homeprovidername-mbnprofile-element.md)           | [**providerNameType**](schema-providernametype-simpletype.md) | Nome do provedor de home.<br/>                     |
| [**ICONFilePath**](schema-iconfilepath-mbnprofile-element.md)                   | [**iconFileType**](schema-iconfiletype-simpletype.md)         | Caminho para o arquivo de ícone.<br/>                         |
| [**IsDefault**](schema-isdefault-mbnprofile-element.md)                         | booleano                                                        | Se o perfil é o padrão.<br/>            |
| [**Nome**](schema-name-mbnprofile-element.md)                                   | [**nameType**](schema-nametype-simpletype.md)                 | Nome do perfil.<br/>                           |
| [**ProfileCreationType**](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | Informações sobre o criador de perfil.<br/>         |
| [**SimIccID**](schema-simiccid-mbnprofile-element.md)                           | [**simIccIDType**](schema-simiccidtype-simpletype.md)         | Número de identificação do SIM para dispositivos GSM.<br/>     |
| [**SubscriberID**](schema-subscriberid-mbnprofile-element.md)                   | [**subscriberIdType**](schema-subscriberidtype-simpletype.md) | Identificador exclusivo do perfil.<br/>              |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



 

 




