---
description: Especifica o padrão de LAN sem fio 802.11 usado em uma LAN sem fio.
ms.assetid: 19582ff0-59bd-4c93-8c92-0135e6e025d2
title: Elemento phyType (conectividade)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- phyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d7f9af94923f9160d18a9787b61036d5cf4104aede6488e2219b18a84325da46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684016"
---
# <a name="phytype-connectivity-element"></a>Elemento phyType (conectividade)

O elemento phyType (conectividade) especifica o padrão de LAN sem fio 802.11 usado em uma LAN sem fio.

Você pode especificar vários **phyType** s. Se nenhum **phyType** for especificado, o perfil poderá ser usado para se conectar a **qualquer phyType**. O valor "n" só tem suporte no Windows Vista com Service Pack 1 (SP1) e versões posteriores do sistema operacional.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Não há suporte para esse elemento.

``` syntax
<xs:element name="phyType"
    minOccurs="0"
    maxOccurs="4"
>
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="a"
             />
            <xs:enumeration
                value="b"
             />
            <xs:enumeration
                value="g"
             />
            <xs:enumeration
                value="n"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento é definido pelo [**elemento de conectividade.**](wlan-profileschema-connectivity-msm-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Conectividade**](wlan-profileschema-connectivity-msm-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**conectividade (MSM)**](wlan-profileschema-connectivity-msm-element.md)
</dt> </dl>

 

 




