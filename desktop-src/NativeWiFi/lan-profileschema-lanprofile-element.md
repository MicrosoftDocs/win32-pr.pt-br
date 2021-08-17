---
description: Contém um perfil de rede com fio.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Elemento LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6adaa0f4884ad275137a6c949dbc466416006f33bb6603dc61e87153d9b23361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065096"
---
# <a name="lanprofile-element"></a>Elemento LANProfile

O elemento LANProfile contém um perfil de rede com fio. Esse elemento é o elemento raiz exclusivo para um perfil de rede com fio.

O namespace de destino para o elemento LANProfile é `https://www.microsoft.com/networking/LAN/profile/v1` .

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="MSM">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="security">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OneXEnforced"
                                        type="boolean"
                                     />
                                    <xs:element name="OneXEnabled"
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
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



| Elemento                                                                 | Type    | Descrição                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msm**](lan-profileschema-msm-lanprofile-element.md)                 |         | Contém configurações de MSM (módulo específico de mídia). <br/>                                                                               |
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | booleano | Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | booleano | Especifica se o serviço de configuração automática para redes com fio requer o uso de 802.1X para autenticação de porta. <br/> |
| [**Segurança**](lan-profileschema-security-msm-element.md)              |         | Contém configurações de segurança. <br/>                                                                                                  |



## <a name="remarks"></a>Comentários

Para exibir a lista de elementos filho em uma estrutura como árvore, consulte Elementos de [ \_ esquema do perfil lan.](lan-profileschema-elements.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



 

 




