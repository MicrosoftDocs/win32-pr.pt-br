---
description: Contém várias configurações para fornecedores de hardware independentes.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Elemento IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789515"
---
# <a name="ihv-wlanprofile-element"></a>Elemento IHV (WLANProfile)

O elemento IHV (WLANProfile) contém várias configurações para fornecedores de hardware independentes. Se um perfil incluir configurações de segurança de IHV, eles substituirão qualquer segurança definida pela Microsoft.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
                type="boolean"
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

O elemento é definido pelo elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**conectividade**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contém configurações de conectividade relacionadas a IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contém um hexBinary de 3 bytes que identifica o IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifica o IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**segurança**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contém configurações de segurança específicas de IHV. As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas. O perfil inteiro será inválido se ambas as configurações de segurança estiverem presentes.<br/>                                                                                                                                                                                            |
| [**Escreva**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contém um hexBinary de 1 byte que é usado para diferenciar NICs pelo mesmo IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [booleano](/dotnet/api/system.boolean) | Especifica a origem das configurações de segurança 802.1 X usadas por um componente de segurança do IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) é verdadeiro, os componentes de segurança de IHV usam configurações 802.1 x definidas pela Microsoft. Quando **useMSOneX** é false, os componentes de segurança de IHV usam configurações 802.1 x fornecidas pelo fornecedor. Por padrão, **useMSOneX** é false. Esse elemento é opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
