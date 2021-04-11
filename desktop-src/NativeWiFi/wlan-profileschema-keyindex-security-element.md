---
description: Especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio. Isso só é usado quando KeyType está definido como &\# 0034; networkKey&\# 0034;.
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: Elemento KeyIndex (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091765"
---
# <a name="keyindex-security-element"></a>Elemento KeyIndex (Security)

O elemento KeyIndex (Security) especifica qual índice de chave deve ser usado para criptografar o tráfego sem fio. Isso só é usado quando [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) está definido como "networkKey".

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                |
| Redistribuível<br/>          | API de LAN sem fio para Windows XP com SP2<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**segurança**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**segurança (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




