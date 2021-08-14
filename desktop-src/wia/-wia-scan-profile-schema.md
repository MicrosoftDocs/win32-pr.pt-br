---
description: o esquema do perfil de verificação define um formato XML que pode ser usado para armazenar as propriedades de itens de aquisição de imagem Windows (WIA), como scanners e câmeras.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Esquema do perfil de verificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81091e75269206b6b3b5a89f86c6f92da5c1d2080d90382ac6af48c6d1cc32ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208012"
---
# <a name="scan-profile-schema"></a>Esquema do perfil de verificação

o esquema do perfil de verificação define um formato XML que pode ser usado para armazenar as propriedades de itens de aquisição de imagem Windows (WIA), como scanners e câmeras. Esses arquivos persistentes permitem que os aplicativos forneçam verificação automática sem exigir que os usuários se lembrem das configurações de propriedade dos itens.

Qualquer dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) pode ter um perfil de verificação. No entanto, **IWiaItem2** itens dos \_ tipos \_ grupo WIA concluído \_ arquivo e \_ raiz da categoria WIA \_ não podem ter perfis.

Os perfis de verificação são criados e gerenciados por meio das interfaces [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)e [**IScanProfileUI**](-wia-iscanprofileui.md) . Os usuários do seu aplicativo podem modificar perfis de maneiras limitadas usando o método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Todos os perfis de verificação têm os seguintes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` e `<Properties>` . O perfil padrão de um dispositivo também tem um `<Default>` elemento.

O `<ProfileGUID>` elemento e o `<DeviceID>` elemento não podem ser alterados depois que o perfil de verificação é criado. Os valores do `<ProfileName>` elemento e do `<WiaItem>` elemento podem ser modificados. O `<Default>` elemento pode ser adicionado ou excluído. Isso pode ser feito de forma programática usando os métodos [**IScanProfile:: SetName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) . Essas propriedades também podem ser alteradas pelos usuários por meio do método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

O `<Properties>` elemento contém `<Property>` filhos. Use-os para adicionar qualquer item WIA ou propriedade de dispositivo ao perfil. Você também pode desenvolver sua própria imagem aquisição `<Property>` filhos. Isso torna o esquema do perfil de verificação extensível. (Para obter mais informações sobre como estender o esquema, consulte [definindo propriedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).)

Aqui está o esquema completo do perfil de verificação. Segue um exemplo de perfil.


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



Clique em **Mostrar exemplo** para ver um perfil de exemplo.


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Constantes da propriedade WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Definindo propriedades personalizadas](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



