---
description: Especifica o número de tentativas de pré-autenticação para tentar em APs vizinhos.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Elemento preAuthThrottle (segurança)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501556"
---
# <a name="preauththrottle-security-element"></a>Elemento preAuthThrottle (segurança)

O elemento preAuthThrottle (segurança) especifica o número de tentativas de pré-autenticação para tentar em APs vizinhos. Esse elemento é válido somente para redes definidas por WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado". Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o número de tentativas padrão será 3.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para este elemento.

``` syntax
<xs:element name="preAuthThrottle"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="16"
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

 

 




