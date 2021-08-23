---
description: Especifica o número de tentativas de pré-autenticação para experimentar APs vizinhos.
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
ms.openlocfilehash: 8bc310d19126a0e4bc9a7e6abf2a6ae1d0eb917cb5f425796d10bee66ea6ebed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064596"
---
# <a name="preauththrottle-security-element"></a>Elemento preAuthThrottle (segurança)

O elemento preAuthThrottle (segurança) especifica o número de tentativas de pré-autenticação para tentar em APs vizinhos. Esse elemento é válido somente para redes definidas pelo WPA2 com [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) definido como "habilitado". Se **PMKCacheMode** estiver habilitado e esse elemento estiver ausente, o número de tentativas será padrão como 3.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.

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

 

 




