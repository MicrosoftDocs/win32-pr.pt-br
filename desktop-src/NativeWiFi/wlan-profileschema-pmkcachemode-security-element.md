---
description: Indica se o cache PMK será usado.
ms.assetid: 5650c893-6047-4e99-a2be-22722d6a809a
title: Elemento PMKCacheMode (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PMKCacheMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 23e32d7a658e41f80eb2a4d8d743afc2c96f7a5a1b4135e646374b98e6acac26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619252"
---
# <a name="pmkcachemode-security-element"></a>Elemento PMKCacheMode (segurança)

O elemento PMKCacheMode (segurança) indica se o cache PMK será usado. Esse elemento é válido somente para redes definidas pelo WPA2. O cache PMK é descrito na [especificação 802.11i.](https://standards.ieee.org/findstds/standard/802.11i-2004.html)

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.

``` syntax
<xs:element name="PMKCacheMode"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="disabled"
             />
            <xs:enumeration
                value="enabled"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo [**elemento de**](wlan-profileschema-security-msm-element.md) segurança.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Segurança**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**security (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




