---
description: Contém uma política de LAN sem fio.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Elemento WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091013"
---
# <a name="wlanpolicy-element"></a>Elemento WLANPolicy

O elemento **WLANPolicy** contém uma política de LAN sem fio. Esse é o elemento raiz exclusivo para um perfil de política sem fio.

O namespace de destino para o elemento **WLANPolicy** é `https://www.microsoft.com/networking/WLAN/policy/v1` .

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="globalFlags">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="enableAutoConfig"
                            type="boolean"
                         />
                        <xs:element name="showDeniedNetwork"
                            type="boolean"
                         />
                        <xs:element name="allowEveryoneToCreateAllUserProfiles"
                            type="boolean"
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
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
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
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



| Elemento                                                                                                                    | Type                                                                     | Descrição                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**allowEveryoneToCreateAllUserProfiles**](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | booleano                                                                  | Especifica se qualquer usuário pode criar um perfil de todos os usuários. <br/>                                                               |
| [**Lista**](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | A lista de redes LAN sem fio às quais qualquer computador deve ter permissão para se conectar. <br/>                                       |
| [**Bloqueios**](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | A lista de redes LAN sem fio às quais um computador não deve se conectar.<br/>                                                    |
| [**denyAllESS**](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | booleano                                                                  | Especifica se o acesso a todas as redes de infraestrutura está bloqueado. <br/>                                                           |
| [**denyAllIBSS**](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | booleano                                                                  | Especifica se o acesso a todas as redes ad hoc está bloqueado. <br/>                                                                   |
| [**ndescrição**](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [**nometype**](wlan-policyschema-nametype-simpletype.md)                | A descrição de uma política de LAN sem fio. <br/>                                                                                |
| [**enableAutoConfig**](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | booleano                                                                  | Especifica se os computadores usam o serviço interno de configuração automática (autoconfiguração) para gerenciar conexões sem fio. <br/> |
| [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | Contém as configurações globais para o módulo de configuração automática (ACM). <br/>                                                    |
| [**nomes**](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [**nometype**](wlan-policyschema-nametype-simpletype.md)                | O nome de uma política de LAN sem fio. <br/>                                                                                       |
| [**rede**](wlan-policyschema-network-allowlist-element.md)                                                             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Uma rede permitida. <br/>                                                                                                      |
| [**rede**](wlan-policyschema-network-blocklist-element.md)                                                             | [**networkitemtype**](wlan-policyschema-networkitemtype-complextype.md) | Uma rede bloqueada. <br/>                                                                                                       |
| [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | A lista de redes permitidas e negadas.<br/>                                                                                  |
| [**ProfileList**](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | Contém uma lista de perfis a serem aplicados no nível de domínio ou computador. <br/>                                                |
| [**showDeniedNetwork**](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | booleano                                                                  | Especifica se as redes negadas aparecem no assistente **conectar-se a uma rede** . <br/>                                         |



## <a name="remarks"></a>Comentários

Para exibir a lista de elementos filho em uma estrutura do tipo árvore, consulte [ \_ elementos do esquema da política de WLAN](wlan-policyschema-elements.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 




