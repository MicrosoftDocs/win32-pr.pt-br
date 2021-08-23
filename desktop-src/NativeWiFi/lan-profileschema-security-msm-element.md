---
description: Contém configurações de segurança para redes com fio.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Elemento Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 8f66021f61536e8c8f09663e9ec2513b11d1ec87829f5c100b48cbf15d98cdd2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685056"
---
# <a name="security-msm-element-lan_policy"></a>Elemento Security (MSM) (LAN_policy)

O elemento Security (MSM) contém configurações de segurança para redes com fio. Esse elemento é opcional.

``` syntax
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
```

O elemento **Security** é definido pelo elemento [**msm**](lan-profileschema-msm-lanprofile-element.md) .

## <a name="child-elements"></a>Elementos filho



| Elemento                                                                 | Type    | Descrição                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md)   | booleano | Especifica se o serviço de configuração automática para redes com fio tentará a autenticação de porta usando 802.1 X. <br/>      |
| [**OneXEnforced**](lan-profileschema-onexenforced-security-element.md) | booleano | Especifica se o serviço de configuração automática para redes com fio requer o uso do 802.1 X para autenticação de porta. <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**MSM**](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**MSM (LANProfile)**](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




