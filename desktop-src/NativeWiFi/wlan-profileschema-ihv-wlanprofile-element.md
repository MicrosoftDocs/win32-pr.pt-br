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
ms.openlocfilehash: 1cfcd9ee463ef91d04d0bebbeac800d48da32fdd777edc2a08ccf0051410160d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799916"
---
# <a name="ihv-wlanprofile-element"></a>Elemento IHV (WLANProfile)

O elemento IHV (WLANProfile) contém várias configurações para fornecedores de hardware independentes. Se um perfil incluir configurações de segurança de IHV, eles substituirão qualquer segurança definida pela Microsoft.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.

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

O elemento é definido pelo [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectividade**](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | Contém configurações de conectividade relacionadas ao IHV.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | Contém um hexBinary de 3 byte que identifica o IHV.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | Identifica o IHV.<br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [**Segurança**](wlan-profileschema-security-ihv-element.md)         |                                                                   | Contém configurações de segurança específicas do IHV. As configurações de segurança da Microsoft e as configurações de segurança de IHV são mutuamente exclusivas. O perfil inteiro será inválido se ambas as configurações de segurança estão presentes.<br/>                                                                                                                                                                                            |
| [**Tipo**](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | Contém um hexBinary de 1 byte que é usado para diferenciar NICs pelo mesmo IHV.<br/>                                                                                                                                                                                                                                                                                                        |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)       | [booleano](/dotnet/api/system.boolean) | Especifica a origem das configurações de segurança 802.1X usadas por um componente de segurança IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) é true, os componentes de segurança IHV usam configurações 802.1X definidas pela Microsoft. Quando **useMSOneX** é false, os componentes de segurança IHV usam configurações 802.1X fornecidas pelo fornecedor. Por padrão, **useMSOneX** é false. Esse elemento é opcional.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



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

 

 
