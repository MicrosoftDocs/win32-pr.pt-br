---
description: Contém configurações do módulo de mídia específica (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Elemento MSM (LANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 25334050e95ff20cf35ed1071bf2b1c006e29c0f9374923199a96c09bbae0471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065076"
---
# <a name="msm-lanprofile-element"></a>Elemento MSM (LANProfile)

O elemento MSM (LANProfile) contém configurações do módulo de mídia específica (MSM).

``` syntax
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
```

O elemento **msm** é definido pelo elemento [**LANProfile**](lan-profileschema-lanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                 | Type    | Descrição                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | booleano | Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X.<br/>       |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | booleano | Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta. <br/> |
| [**segurança**](lan-profileschema-security-msm-element.md)              |         | Contém configurações de segurança. <br/>                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**LANProfile**](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




