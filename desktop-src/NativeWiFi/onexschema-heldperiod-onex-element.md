---
description: Especifica o período de tempo, em segundos, em que um cliente não tentará a autenticação de novo após uma tentativa de autenticação com falha.
ms.assetid: a6b32e88-da36-4aea-a01d-f5f7bc37d171
title: Elemento heldPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- heldPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5a2009ac8518d114353e3323b97c4ea57c54fc801447c375641b8f6bbd1b2bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684846"
---
# <a name="heldperiod-onex-element"></a>Elemento heldPeriod (OneX)

O elemento heldPeriod (OneX) especifica o período de tempo, em segundos, no qual um cliente não tentará a autenticação de novo após uma tentativa de autenticação com falha.

Esse elemento é opcional. Quando heldPeriod não é especificado em um perfil, um valor de 1 segundo é usado.

**Windows XP com SP3 e API de LAN sem fio para Windows XP com SP2:** Esse elemento será ignorado se estiver presente em um perfil.

``` syntax
<xs:element name="heldPeriod">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="3600"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O **elemento heldPeriod** é definido pelo [**elemento OneX.**](onexschema-onex-element.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Onex**](onexschema-onex-element.md)
</dt> </dl>

 

 




