---
description: Especifica as informações de configuração 802.1 X para um perfil de LAN com ou sem fio.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Elemento OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778711"
---
# <a name="onex-element"></a>Elemento OneX

O elemento OneX especifica informações de configuração 802.1 X para um perfil de LAN com ou sem fio. Esse é o elemento raiz exclusivo para um perfil 802.1 X.

O namespace de destino para o elemento OneX é `https://www.microsoft.com/networking/OneX/v1` . A maioria dos elementos filho do elemento OneX está no `OneX` namespace. Há uma exceção: o elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) está no `https://www.microsoft.com/provisioning/EapHostConfig` namespace.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Somente o elemento [**EAPConfig**](onexschema-eapconfig-onex-element.md) tem suporte. Outros elementos, se presentes em um perfil, serão ignorados.

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="100"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
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



| Elemento                                                                            | Type    | Descrição                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthMode**](onexschema-authmode-onex-element.md)                               |         | Especifica o tipo de credenciais usadas para autenticação.<br/>                                                                                                                                                        |
| [**authPeriod**](onexschema-authperiod-onex-element.md)                           |         | Especifica o período máximo de tempo, em segundos, no qual um cliente aguarda uma resposta do autenticador.<br/>                                                                                                  |
| [**cacheUserData**](onexschema-cacheuserdata-onex-element.md)                     | booleano | Especifica se as credenciais do usuário são armazenadas em cache para as conexões subsequentes.<br/>                                                                                                                                     |
| [**EAPConfig**](onexschema-eapconfig-onex-element.md)                             |         | Especifica a configuração do EAPHost.<br/>                                                                                                                                                                              |
| [**heldPeriod**](onexschema-heldperiod-onex-element.md)                           |         | Especifica o período de tempo, em segundos, no qual um cliente não tentará realizar a autenticação novamente após uma tentativa de autenticação com falha.<br/>                                                                             |
| [**maxAuthFailures**](onexschema-maxauthfailures-onex-element.md)                 |         | Especifica o número máximo de falhas de autenticação permitidas para um conjunto de credenciais.<br/>                                                                                                                         |
| [**maxDelay**](onexschema-maxdelay-singlesignon-element.md)                       |         | Especifica, em segundos, o atraso máximo antes da tentativa de conexão de logon único falhar.<br/>                                                                                                                      |
| [**maxStart**](onexschema-maxstart-onex-element.md)                               |         | Especifica o número máximo de EAPOL-Start mensagens enviadas.<br/>                                                                                                                                                        |
| [**Logon único**](onexschema-singlesignon-onex-element.md)                       |         | Especifica as informações de configuração de rede de logon único.<br/>                                                                                                                                                       |
| [**startPeriod**](onexschema-startperiod-onex-element.md)                         |         | Especifica o período de tempo, em segundos, a aguardar antes que um EAPOL-Start seja enviado.<br/>                                                                                                                                  |
| [**suplicable**](onexschema-supplicantmode-onex-element.md)                   |         | Especifica o método de transmissão usado para pacotes EAPOL.<br/>                                                                                                                                                      |
| [**Escreva**](onexschema-type-singlesignon-element.md)                               |         | Especifica quando o logon único é executado. Quando definido como `preLogon` , o logon único é executado antes de o usuário fazer logon. Quando definido como `postLogon` , o logon único é executado imediatamente após o usuário fazer logon.<br/> |
| [**userBasedVirtualLan**](onexschema-userbasedvirtuallan-singlesignon-element.md) | booleano | Especifica se a LAN virtual (VLAN) usada pelo dispositivo é alterada com base nas credenciais do usuário.<br/>                                                                                                                   |



## <a name="remarks"></a>Comentários

Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [elementos do esquema Onex](onexschema-elements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



 

 




