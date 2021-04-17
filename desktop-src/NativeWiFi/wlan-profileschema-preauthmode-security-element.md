---
description: Indica se a pré-autenticação será usada pelo cliente.
ms.assetid: 305d77b6-fe2d-45c6-ac91-5769f91de152
title: Elemento preAuthMode (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ac74f193fb89c260b1a121b673f239147658865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775678"
---
# <a name="preauthmode-security-element"></a>Elemento preAuthMode (Security)

O elemento preAuthMode (Security) indica se a pré-autenticação será usada pelo cliente. A pré-autenticação é necessária para o roaming rápido seguro do WPA2. Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado". Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o valor padrão será "Disabled".

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.

``` syntax
<xs:element name="preAuthMode"
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

O elemento é definido pelo elemento [**Security**](wlan-profileschema-security-msm-element.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 




